+++
title = "DIY: Site web"

math = true

type = "remark"
theme = "uo"


+++
class: center, middle, inverse

# Git: Why and how?

10th January 2019

*Usage: perso, séminaire, équipe, logiciel, documentation logiciel, cours, ~~faire le café~~...*

MÀJ : 29 octobre 2018

---
# Pourquoi avoir son site perso ?

- *~~Parce que tout le monde en a un~~*
- Visibilité :
  - De vous
  - De votre travail
- Accès à vos publications
- Enseignement :
  - Listing
  - Horaires / Salles
  - Cours (plutôt qu'un pdf)
- Informations pour vous contacter
- Liens vers vos projets (ANR, Équipe Inria, ...)
- CV

---
## Méthode actuelle : héritage

> *Tiens, voilà le code séculaire qui te permet d'avoir un site.*
> *Surtout, ne change rien, celui qui a codé cela est maintenant à la retraite...*

- Maintenance laborieuse (si existante)
- Non "responsive" (mobile / tablette )
- [possibles] Failles de sécurité
- Design parfois douteux


## Développement web : c'est un métier...


- Nombreux Langages :
  - HTML (sémantique)
  - CSS ("design")
  - JavaScript (horrible)
- Veille technologique 
  - Framework (Bootstrap, ...)
  - Bibliothèques (Javascript (ou pas))
  - ...
- Accessibilité

---
class:center, middle

# En résumé...

<iframe src="https://giphy.com/embed/5eFp76zhsq3uw" width="720" height="477" frameBorder="0" ></iframe>

---
class:center
# Alors, que faire ?
<iframe src="/img/talks/website/mr-manatane-comprendre-la-jeunesse.jpg" width="720" height="477" frameBorder="0" ></iframe>

---
class:inverse, center, middle

# Ce qu'on vous propose

*Sans connaître une once de HTML et encore moins de Javascript !*

---

## Séparer contenu et mise en page

1. Déléguer aux personnes compétentes la **technique** et le **design**

2. Se concentrer sur le **contenu** (notre *valeur ajouté*)


| Avantages | Désavantages |
| ---- | ------------ |
| Technologie à jour | "Prisonnier" du template |  
|  Solution "clé en main"    | "Standardisation" |  


## Remarques

1. Le contenu ne dépend pas du thème (*aux méta-données près*)
2. Similaire à LaTeX : séparation contenu / mise en page (design)

---

## Contenu 
### Des Méta-données

```toml
+++
...
name = "Batman"
role = "Justicier masqué"
organizations = [ { name = "Wayne Enterprises", url = "#" } ]
...
+++
```
### Du Markdown ("LaTeX en plus simple")

Exemple de fichier Markdown `.md` ([Plus d'info](https://fr.wikipedia.org/wiki/Markdown)
) :

```markdown
# Section
## SubSection
### SubSubSection
Je **suis en gras**
Tu es en *italique*
[Ceci est un lien vers url](url)
Voilà des math :$x = 2$
```

---
## Thème : [Hugo-Academic](https://github.com/gcushen/hugo-academic) pensé pour les académiques 

1. Contient **l'agencement** du code HTML (*layout*) et le **design** (CSS)

2. Design modern et **responsive**, code **maintenu** (en tout cas en 2018)

3. Fonctionnalités :

    - "About" : 
      - CV / Domaine d'intérêt / Bio / ...
      - Liens "sociaux" (researchgate, google scholar, github, ...)
    - Listes de vos ...
      - Publications + lien vers pdf/DOI/code/slides/projet/...
      - Talks + lien vers pdf/DOI/code/slides/projet/...
    - Pages pour vos 
        - Projets (ANR, ERC, ...)
        - Enseignements
    - Informations pour vous contacter
    - Cours / Documentation logicielle
    - Cadeau bonus : LaTeX
  $$\int\_{\Omega} u(x) = 1$$

---
## Moteur : Hugo (générateur de sites statiques)

- **Transforme** le code Markdown en code HTML **selon le thème**
- Séparation du code (`.md`) et du résultat (`.html`)
- *Un peu comme LaTeX qui sépare le code (`.tex`) du résultat (`.pdf`)*

<iframe src="/img/talks/website/hugo.png" width="800" height="500" frameBorder="0" ></iframe>


---
### Arborescence/Structure du code "forcé" et pré-déterminé



```toml
.
├── config.toml      # Vos paramètres globaux
├── content          # Vos contenus
    └── home           # Homepage
    └── publication    # Vos publis
          └── publi1       # publi 1
               └── index.md       # fichier principal
               └── featured.jpg   # image illustration
               └── publi1.pdf     # pdf
               └── publi1.bib     # bibtex
          └── publi2       # publi 2
          └── ...          
    └── talks          # Vos talks
    └── projects       # Vos projets
    └── courses        # Vos cours
    └── ...    
├── data           # Données (tableau, ...)
├── layouts        # Vos layouts persos
├── static         # Vos fichiers annexes (images, ...)
    └── css        # Vos fichiers css persos
    └── img        # Vos images
└── themes         # Code du thème : SURTOUT Ne Pas toucher !
    └── academic      
          └── exampleSite # Exemples pratiques
          └── ...
```


---
class:inverse,middle,center

# Installation
*Vite fait bien fait*

---
## All you need is ~~love~~ Hugo ...

### Mac OS (installez [brew](https://brew.sh/))

```bash
brew update        # Mise à jour de la base de données
brew install hugo  # Installer Hugo (une fois pour toute)
```
Pour mettre à jour Hugo :
```bash
brew update       # Mise à jour de la base de données
brew upgrade      # Mise à jour des logiciels
```

### Linux / Windows (/ Mac OS)

1. [Téléchargez le dernier binaire](https://github.com/gohugoio/hugo/releases)
2. Placez le dans un dossier accessible "partout", *e.g.* `/opt/hugo/hugo`
3. Remarques :
  - ⚠ Package Linux `hugo` obsolète ! À éviter ! ⚠ 
  - Compilation possible (⚠ dernière version de Go)


---

## .. And the Theme Sources

[Issue de la documentation](https://github.com/sourcethemes/academic-kickstart#quick-install-using-your-web-browser)

### Fortement recommandé : avec Git

- Git : "*une fois pour toute*", non obligatoire pour la suite
- Remarque : le nom du dossier  `webpage` est un choix perso

```bash
git clone https://github.com/sourcethemes/academic-kickstart.git webpage
cd webpage
git submodule update --init --recursive
```


### Moins recommandé : à la main (mises à jour futures compliquées)

Téléchargez et dézippez :
- [Base du thème](https://github.com/sourcethemes/academic-kickstart/archive/master.zip) dans `webpage` (par ex.)
- [Source du thème](https://github.com/gcushen/hugo-academic/archive/master.zip) dans `webpage/themes/academic`


---

## Générez le site localement

1. Lancez le serveur Hugo dans un terminal (et laissez le tranquille !) :
```bash
cd Dossier/Du/Site
hugo serve
```
2. Naviguez sur [http://localhost:1313](http://localhost:1313)
3. Mise à jour automatique du code, rafraichissez la page web


## Déployez votre site sur le serveur
- Générez votre site (*construit un dossier `public`*):
```bash
hugo
```
- Déployez le sur le serveur du labo (évitez la commande `scp`) :
```bash
rsync -avz --delete public/ username@web.ljll.math.upmc.fr:~/public_html
```

> *La commande est barbare mais il suffit de la copier/coller*

---
## Vous devriez avoir ceci :

<iframe src="/img/talks/website/lena.png" width="800" height="500" frameBorder="0" ></iframe>


---
class: middle, inverse, center
# Gérer le contenu ([source](https://sourcethemes.com/academic/docs/managing-content/d))
*Parce que bon s'appeler Lena Smith c'est drôle 2 minutes...*
---

## Votre photo

1. "Petite" taille : `400px` x `400px` est suffisant
2. Placez la dans `/static/img/portrait.jpg` (⚠ gardez le même nom)
3. [Possible] Relancez le serveur `hugo` (`CTRL + C` et `hugo serve`)

## Options globales du site : `/config.toml`

1. `TomL`: Un commentaire est précédé du signe `#`
2. Remplissez les cases qu'il convient (`name`, ...)
3. Le menu principal est ici :

```toml
[[menu.main]]
  name = "Home"
  url = "#about"
  weight = 1     # Les plus légers en premiers, les plus lourds à la suite
[[menu.main]]
  name = "Mon Ajout"
  url = "lien_vers_cette_page"
  weight = 10
```
---
## Le contenu ? Dans `content/...`

1. Chaque fichier Markdown (`.md`) sera transformé en `.html`
2. Sauf mention contraire : `content/truc/machin.md` devient `monsite.com/truc/machin.html`
3. Chaque fichier `.md` possède :
  - une en-tête avec les **méta-données** (*e.g* `authors`) séparé par `+++`
  - le contenu en MarkDown
4. Pour ne pas "transformer" un fichier en `html` :
  - ~~Supprimer le~~
  - Modifiez la méta-donné  : 
      - `draft = true`
      - ou (pour les widgets de `home`) : `active = false`

```markdown
+++
# About/Biography widget.
widget = "about"
active = false
date = 2016-04-20T00:00:00

# Order that this section will appear in.
weight = 5
+++

Contenu : Je suis vraiment un geek

```

---
## Homepage divisée en widgets : `content/home/`


### Arborescence 

```toml
.
├── content          # Vos contenus
    └── home            # Homepage
          └── about.md          # Bio
          └── contact.md        # Contact info
          └── features.md       # Fonctionnalités (pour un logiciel)
          └── hero_carousel.md  # Images bannières du site défilantes
          └── hero.md           # Image bannière du site
          └── posts.md          # Vos posts (blog)
          └── projects.md       # Vos projets
          └── publications_selected.md # Vos publis mises en avant
          └── publications.md   # Listing de vos publications
          └── search.md         # bouton "rechercher"
          └── skills.md         # Compétences
          └── tags.md           # Tags du site (recherche "horizontale")
          └── talks.md          # Listing de vos présentations
          └── ...            
```
Remarque : le "html" des Widgets est dans `/themes/academic/layouts/partials/widgets`

---

### Widgets usuels

- Majoritairement à **contenu "vide"** mais remplis de **méta-données**
- Choisi dans les méta-données
- Le widget `custom` permet d'afficher simplement ce que vous voulez

```toml
+++
...
widget = "custom"          # <---- Choix du widget 
active = true             # <---- Publié ou non ?
date = 2016-04-20T00:00:00 #<- Ne sera pas publié si date dans futur
...
+++
```


### Widget page

- Créer une page avec [ses propres "widgets"](https://sourcethemes.com/academic/docs/managing-content/#create-a-widget-page) (comme la homepage) est possible

---

## Publications : `/content/publication`

### Arborescence 

Une publication = un dossier

```toml
.
├── config.toml      # Vos paramètres globaux
├── content          # Vos contenus
    └── home            # Homepage
    └── publication       # publis
          └── publi1         # publi 1
               └── index.md       # fichier 
               └── featured.jpg   # image illustration
               └── publi1.pdf     # pdf
               └── publi1.bib     # bibtex
          └── publi2         # publi 2
          └── ...          
```

---
### Nouvelle publication

#### Depuis un fichier .bib

Avec [Academic Admin](https://github.com/sourcethemes/academic-admin) (non testé !)

#### Simple mais efficace

Copiez/Collez dans `content/publication/fourier64/index.md`
  - Une public existante à vous 
  - Ou dans `/themes/academic/exampleSite/content/publication/` 

#### Mieux mais buggué (waiting for Hugo 0.50)

```bash
hugo new --kind publication publication/<my-publication>
```
---

### Méta-données

- `authors`
- `publication_types`
- `publication` (=nom du journal)
- `selected` : Mise en avant (widget "*publication_selected*") ?
- `url_XXX` : lien vers `XXX` (pdf, slide, projet, ...)
- `doi` : renseignez le numéro DOI
- `math = false` : Autoriser LaTeX dans le contenu (laisser `false` si non)
- `[image]` : image d'illustration (`featured.jpg`)

### BibTeX, Pdf et image ?

Dans le dossier de la publi, placez :

- Fichier `.bib` (peu importe le nom)
- Document `.pdf` avec le même nom que le dossier
- Une image `featured.jpg` (ratio plutôt 1600x400)

### Remarque : similaire pour les talks

---
## Listing des publications/talks/projects/...

```
https://votresite.com/projects
https://votresite.com/talks
https://votresite.com/publications
```

Le listing avec toutes vos publications est fourni avec un système de filtre...

<iframe src="/img/talks/website/listing.png" width="720" height="477" frameBorder="0" ></iframe>


---
## Projecteur sur le Widget Projects

- Affichage par "cards" plutôt agréables
- Réutilisable. Exemple pour l'enseignement :

```toml
# Fichier content/home/teaching.md
+++
# Projects widget.
widget = "projects"         # Choix du widget projects
active = true
date = 2016-04-20T00:00:00

title = "Teaching"          # Nom à afficher sur la Homepage
subtitle = ""               # sous titre

# Order that this section will appear in.
weight = 60

# Content.
# Display content from the following folder.
# For example, `folder = "project"` displays content from `content/project/`.
folder = "teaching"
...

```
---
## *Layout* d'une page web

### Layouts fournis

`post` (blog), `publication`, `talk`, `project`, `docs` (doc logiciel / cours) 

### Définir le layout d'une page

- Choix automatique selon le nom du dossier ...
> Dossier `content/publication` implique layout `publication`
- ... Ou forcé dans l'en-tête
```toml
+++
...
type = "docs"  # par exemple !
...
+++
```
---


class: middle, center, inverse
# Allez plus loin
*Vers l'automatisation et au-delà*

---
## Read The Nice Manual

- [Documentation très (très) exhaustive](https://sourcethemes.com/academic/docs/) et maintenue (sisi !) notamment la partie [Writing your content](https://sourcethemes.com/academic/docs/writing-markdown-latex/)
- Jetez un coup d'oeil dans `/themes/academic/exampleSite`
- Venez nous voir et/ou regardez [les issues](https://github.com/gcushen/hugo-academic/issues)
- [Souscrivez à la mailing list locale](https://listes.math.cnrs.fr/wws/subscribe/hugo-academic?previous_action=info)


## MÀJ du thème (régulièrement mais pas trop !)

```bash
sh ./update_academic.sh
```
1. Re-Téléchargez la dernière version de Hugo
2. Possible "break" !
3. Ne pas le faire le vendredi soir avant de partir en week-end

## Bricoler hors des sentiers battus ?

Possible mais attention à la maintenance

---
## Automatisation avec Git

### Rappels : quelques commandes
- `git status` = statut du dépôt
```bash
git status
```
- `git add` = tracker un nouveau fichier
```bash
git add monfichier
```
- `git commit` = faire une "sauvegarde" du code
```bash
git commit -m "message" -a
```
- `git push` = envoie du code sur le serveur
```bash
git push
```
---

### Services externes : Netlify

- Nécessite un compte [Gitlab.com](https://gitlab.com) ou [gihub](https://github.com) ou [bitbucket](https://bitbucket.org)
- [Netlify](https://app.netlify.com/signup) génère et déploie un site en quelques secondes après votre `push`
- Rediction en plaçant un fichier `.htacess` dans `public_html` :
```bash
Redirect 301 /username https://votresite.netlify.com
```

Remarques : 
- Github : Le code du site sera alors **public**. Demandez alors le [*student developper pack*](https://education.github.com/) (gratuit pour les académiques)
- N'utilisez **surtout pas un email @protonmail.com** (snif)

### En interne avec le Gitlab du labo

En cours !

---
class: middle, center, inverse

# Merci !

<iframe src="https://giphy.com/embed/ClcWrARkrq1GM" width="480" height="260" frameBorder="0" class="giphy-embed" allowFullScreen></iframe>
