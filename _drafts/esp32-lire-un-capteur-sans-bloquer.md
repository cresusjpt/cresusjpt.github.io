---
title: "ESP32 : lire un capteur sans bloquer la boucle"
date: 2026-11-02 09:00:00 +0100
description: "Remplacer delay() par une horloge logicielle : le firmware reste réactif pendant que le capteur travaille."
exemple: true
---

Sur un ESP32 programmé avec le framework Arduino, la tentation est d'écrire :

```cpp
void loop() {
  float t = lireTemperature();
  envoyer(t);
  delay(5000); // le processeur attend 5 s sans rien faire d'autre
}
```

Pendant ces cinq secondes, le firmware n'écoute plus rien : ni le bouton, ni la liaison BLE, ni une mise à jour à distance.

## Une horloge logicielle

`millis()` renvoie le nombre de millisecondes écoulées depuis le démarrage. On mémorise l'instant de la dernière mesure et on compare :

```cpp
const unsigned long PERIODE_MS = 5000;
unsigned long derniereMesure = 0;

void loop() {
  const unsigned long maintenant = millis();
  if (maintenant - derniereMesure >= PERIODE_MS) {
    derniereMesure = maintenant;
    envoyer(lireTemperature());
  }
  traiterBouton();  // toujours réactif
  traiterBle();
}
```

> La soustraction `maintenant - derniereMesure` reste juste quand `millis()` repasse par zéro, au bout d'environ 49 jours, grâce à l'arithmétique non signée.

## Quand passer à FreeRTOS

Au-delà de trois ou quatre tâches périodiques, les comparaisons s'accumulent. L'ESP32 embarque FreeRTOS : une tâche par responsabilité, et `vTaskDelay()` rend la main au lieu de bloquer.

```cpp
void tacheMesure(void *) {
  for (;;) {
    envoyer(lireTemperature());
    vTaskDelay(pdMS_TO_TICKS(5000));
  }
}

void setup() {
  xTaskCreate(tacheMesure, "mesure", 4096, nullptr, 1, nullptr);
}
```
