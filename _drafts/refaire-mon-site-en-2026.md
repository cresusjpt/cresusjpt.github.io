---
title: "Refaire mon site en 2026 : Jekyll, GitHub Pages et zéro serveur"
date: 2026-11-16 10:00:00 +0100
description: "Cinq ans après une première version jamais terminée, je repars d'une feuille blanche en gardant le déploiement le plus simple possible : un push."
---

En 2021, j'ai monté ce site en copiant un thème Jekyll entier dans mon dépôt. Il est resté inachevé : un blog vide, des boutons qui menaient vers des pages 404, un formulaire de contact sans style. Cinq ans plus tard, je le refais avec une règle simple : **publier doit rester aussi simple qu'un `git push`**.

## Ce que je garde

GitHub Pages construit le site à chaque push sur la branche `master`. Pas de serveur à maintenir, pas de facture, HTTPS fourni. Jekyll reste le moteur : une note est un fichier Markdown.

```ruby
# Gemfile : mêmes versions que la construction GitHub Pages
source "https://rubygems.org"
gem "github-pages", group: :jekyll_plugins
gem "webrick"
```

## Ce que je jette

| Avant | Après |
|---|---|
| Le thème complet copié dans le dépôt, documentation et tests compris | Deux gabarits et une feuille de style |
| jQuery et les scripts du thème | Un petit script, sur la page contact seulement |
| Commentaires Disqus | Le formulaire de contact |
| Images d'illustration génériques | Une vue en coupe dessinée en SVG |

## Le domaine sans « www »

`www.jeanpaultossou.tech` pointait bien vers GitHub, mais pas `jeanpaultossou.tech`. Il suffit d'ajouter chez le registraire les quatre enregistrements `A` de GitHub Pages, sans toucher aux enregistrements `MX` de la messagerie :

```text
@    A      185.199.108.153
@    A      185.199.109.153
@    A      185.199.110.153
@    A      185.199.111.153
www  CNAME  cresusjpt.github.io.
```

GitHub redirige ensuite le domaine nu vers `www`.

> Avant de modifier une zone DNS, notez les valeurs existantes. Une erreur sur les `MX` coupe la messagerie, pas le site.

## Publier une note

Une note est un fichier dans `_posts/`, nommé `AAAA-MM-JJ-titre.md` :

```markdown
---
title: "Mon titre"
description: "Une phrase qui résume la note."
---

Le texte, en Markdown.
```

Puis `git add`, `git commit`, `git push`. Une minute plus tard, la note est en ligne, dans le flux RSS et dans le plan du site.
