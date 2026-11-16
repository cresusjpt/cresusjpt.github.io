# jeanpaultossou.tech

Site personnel de Jean-Paul Tossou : présentation, réalisations et notes techniques.
Construit avec Jekyll, publié par GitHub Pages à chaque push sur `master`. Aucun serveur.

## Publier une note

1. Créer `_posts/AAAA-MM-JJ-titre-de-la-note.md` :

   ```markdown
   ---
   title: "Titre de la note"
   description: "Une phrase qui résume la note (liste du blog et partage)."
   ---

   Le texte, en Markdown. Les blocs de code ```cpp sont colorés.
   ```

2. `git add`, `git commit`, `git push`. La note est en ligne une minute plus tard, numérotée automatiquement (NT-001, NT-002…), dans le flux RSS et le plan du site.

Un brouillon se range dans `_drafts/` (sans date dans le nom) : il apparaît en local, jamais en ligne.

## Modifier le contenu

| Quoi | Où |
|---|---|
| Nom, titre, e-mail, liens, lien Saltech, rendez-vous (`rendez_vous`), formulaire (`contact_form`) | `_config.yml` |
| Missions (références) | `_data/missions.yml` |
| Produits (Lockey You, diffuseur) | `_data/projets.yml` |
| Couches de la vue en coupe et nomenclature | `_data/couches.yml` |
| Étude de cas Lockey You | `projets/lockey-you.html` |
| Bloc Saltech (accueil, parcours) | `_includes/saltech.html` |
| Accueil, réalisations, parcours, contact | `index.html`, `projets.html`, `about.html`, `contact.html` |
| Styles (une seule feuille, sans préprocesseur) | `assets/css/site.css` |

`hypotheses: true` dans `_config.yml` affiche des tampons « À valider » et des mentions « À préciser » sur le contenu supposé ou incomplet. Passer à `false` une fois les textes relus.

Règles de rédaction, les mêmes que pour saltech.fr : pas de tiret cadratin, pas de jargon creux, aucun fait inventé. Pour les références, voir l'en-tête de `_data/missions.yml`.

## Prévisualiser en local

Prérequis : Ruby 3 (par exemple `brew install ruby`).

```bash
bundle config set --local path vendor/bundle
bundle install
bundle exec jekyll serve --drafts
```

Puis ouvrir http://localhost:4000. Sur macOS, si l'installation du gem `openssl` échoue :
`bundle config set --local build.openssl "--with-openssl-dir=$(brew --prefix openssl@3)"`.

## Domaine

Le fichier `CNAME` déclare `www.jeanpaultossou.tech`. Pour que `jeanpaultossou.tech` (sans www) fonctionne aussi, le domaine nu doit pointer vers GitHub Pages chez le registraire (enregistrements `A` 185.199.108.153, .109, .110, .111), sans toucher aux enregistrements `MX` de la messagerie.

## Polices

Osifont (lettrage ISO 3098) et Atkinson Hyperlegible Next, auto-hébergées : voir `assets/fonts/LICENSES.txt`.
