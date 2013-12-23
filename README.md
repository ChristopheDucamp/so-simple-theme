# Thème So Simple

Vouc chercher un thème simple, responsive pour votre blog Jekyll ? Bon ne cherchez pas plus loin. Voici  **So Simple Theme**, une relance de [**Minimal Mistakes**](http://mmistakes.github.io/minimal-mistakes/) -- conçue par le designer / illustrateur [Michael Rose](http://mademistakes.com).

## So Simple Theme c'est tout cela :

* Des templates dites "Responsive". Mieux sur mobile, tablettes et desktop.
* Dégradation gracieuse dans les navigateurs les plus vieux. Compatible avec Internet Explorer 9+ et tous les navigateurs modernes.
* Embellissements minimes et animations subtiles.
* Typographie lisible pour faire briller vos mots.
* Support pour les grandes images pour faire ressortir vos posts préférés.
* Commentaires Disqus si vous choisisssez de les autoriser.
* Structure simple et claire des permaliens[^1].
* Tags pours [Open Graph](https://developers.facebook.com/docs/opengraph/) and [Twitter Cards](https://dev.twitter.com/docs/cards) pour une meilleure expérience de partage social.
* Vanilla [page 404 personnalisée]({{ site.url }}/404.html) pour vous faire démarrer.
* Feuilles de style pour Pygments et Coderay [éclairage syntaxe](http://mmistakes.github.io/articles/so-simple-theme/code-highlighting-post/) pour faire que vos exemples de code soient présentés avec élégance.
* Recherche simple qui chevauche les résultats basées sur les titres des posts.
* Script de construction Grunt pour un développement de thème plus facile.
* [Sitemap](https://github.com/mmistakes/so-simple-theme/blob/master/sitemap.xml) pour les moteurs de recherche.

![screenshot de So Simple Theme](http://mmistakes.github.io/so-simple-theme/images/so-simple-theme-preview.jpg)

Notes générales et suggestions pour personnaliser So Simple Theme.

---

## Installation basique pour un nouveau site Jekyll

1. [Installez Jekyll](http://jekyllrb.com) et lisez la documentation si ce n'est déjà fait.
2. Forkez le [dépôt So Simple Theme](https://github.com/mmistakes/so-simple-theme/fork)
3. Clonez le dépôt que vous venez juste de forker.
4. Éditez le fichier `_config.yml` pour personnaliser votre site.
5. Regardez les posts échantillons dans `_posts` pour voir des exemples qui savent extraire de grandes images, en leur assignant des catégories et mots-clés, et d'autres data YAML.
6. Lisez la documentation en-dessous pour plus de personnalisation des pointeurs

[Téléchargez le thème](http://mmistakes.github.io/so-simple-theme)

**Pro-truc :** Effacez la branche `gh-pages` après avoir cloné et commencez fraîchement par la déconnexion de la branche  `master`. Il y a plein de déchets dans `gh-pages` utilisé pour le site de démo du thème dont vous ne voudrez pas sur votre site.

---

## Installation pour un site Jekyll existant

1. Clonez les dossiers suivants : `_includes`, `_layouts`, `assets`, et `images`.
2. Clonez les fichiers suivants et personnalisez le contenu comme souhaité : `about.md`, `articles.html`, `index.html`, `tags.html`, `feed.xml`, et `sitemap.xml`.
3. Réglez les variables suivantes dans votre fichier `config.yml` :

``` yaml
title:            Titre du Site
description:      description du site pour les métas.
logo:             logo-du-site.png
disqus_shortname: shortname
search:           true
#Retirez l'url si vous travaillez localement pour résoudre correctement les urls de base
url:              http://whatever.com

# Propriétaire/information auteur
owner:
  name:           Votre Nom
  avatar:         votre-photo.jpg
  email:          votre@email.com
  # Les liens de silos sociaux utilisés dans le footer. Mettez-les à jour et retirez-les à votre guise.
  twitter:
  facebook:
  github:
  linkedin:
  instagram:
  tumblr:
  # Pour la parternité d'auteur Google +  https://plus.google.com/authorship
  google_plus:    "http://plus.google.com/123123123123132123"

# Les analytics et autres outils de webmaster se rangent ici
google_analytics:
google_verify:
# https://ssl.bing.com/webmaster/configure/verify/ownership Option 2 content= goes here
bing_verify:

# Liens à inclure dans la navigation en haut
# Pour l'ajout de liens externes ajoutez  external: true
links:
  - title: About
    url: /about
  - title: Articles
    url: /articles
  - title: Google
    url: http://google.com
    external: true

# http://en.wikipedia.org/wiki/List_of_tz_database_time_zones
timezone:    America/New_York
pygments:    true
markdown:    kramdown

# https://github.com/mojombo/jekyll/wiki/Permalinks
permalink:   /:categories/:title
```

---

## Structure des dossiers

``` bash
so-simple-theme/
├── _includes/
|    ├── browser-upgrade.html  #alerte pour mise à jour navigateurs  < IE8
|    ├── footer.html  #site footer
|    ├── head.html  #site head
|    ├── navigation.html #site navigation et masthead
|    └── scripts.html  #jQuery, plugins, GA, etc.
├── _layouts/
|    ├── page.html  #page layout
|    └── post.html  #post layout
├── _posts/
├── assets/
|    ├── css/  #preprocessed less styles
|    ├── fonts/  #icon webfonts
|    ├── js/
|    |   ├── _main.js  #main JavaScript file, plugin settings, etc
|    |   ├── plugins  #jQuery plugins
|    |   └── vendor/  #jQuery and Modernizr
|    └── less/
├── images  #images for posts and pages
├── _config.yml  #Jekyll site options
├── about.md  #about page
├── articles.md  #liste tous les posts du plus récent aux plus vieux
├── index.html  #homepage. liste les 10 posts les plus récents
├── tags.html  #lists tous les posts classés par mots-clés
└── sitemap.xml  #sitemap autogénéré pour moteurs de recherche
```

---

## Personnalisation

Pour les détails complets de personnalisation et plus d'information sur le thème regardez le [guide du thème So Simple](http://mmistakes.github.io/so-simple-theme/theme-setup/).

---

## Questions ?

Si vous avez quelque problème à faire fonctionner quelque chose ou si vous voulez savoir pourquoi je paramètre un truc de la sorte ... Pinguez  [@mmistakes](http://twitter.com/mmistakes) sur twitter ou [enregistrez un problème GitHub](https://github.com/mmistakes/so-simple-theme/issues/new).

---

## Licence

Ce thème est un logiciel libre et opensource distribué sous la [GNU General Public License](LICENCE GNU GPL) version 2 ou suivante. Sentez-vous ainsi libre d'utiliser ce thème Jekyll sur votre site sans vous sentir obligé de me faire un lien retour ou d'utiliser un "disclaimer".

Si vous souhaitez me créditer quelque part sur votre blog ou tweeter un message à [@mmistakes](https://twitter.com/mmistakes), ce serait vraiment délicat.
