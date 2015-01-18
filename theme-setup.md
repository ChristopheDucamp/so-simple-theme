---
layout: page
permalink: /theme-setup/index.html
title: Installer le Thème
description: "Instructions pour savoir comment installer et personnaliser le thème Jekyll So Simple."
modified: 2013-12-23
tags: [Jekyll, thème, install, setup, installation, démarrage]
---

Notes Générales et suggestions pour personnaliser le thème **So Simple**.

## Installation Basique pour un Nouveau Site Jekyll

1. [Installez Jekyll](http://jekyllrb.com) et lisez la documentation si vous ne l'avez pas encore fait.
2. Forkez le [dépôt So Simple Theme](https://github.com/mmistakes/so-simple-theme/fork)
3. Clonez le dépôt que vous venez de forker.
4. Éditez `_config.yml` pour personnaliser votre site.
5. Regardez les posts-échantillons dans `_posts` pour voir des exemples à extraire de grandes images, assignant des catégories et tags et autres data YAML.
6. Lisez la documentation en-dessous pour une personnalisation plus poussée.

<div markdown="0"><a href="https://github.com/mmistakes/so-simple-theme" class="btn">Téléchargez le Thème</a></div>

**Pro-truc :** Effacez la branche `gh-pages` après l'avoir clonée et démarrez de zéro en débranchant  `master`. Il y a tout un paquet de déchets dans `gh-pages` utilisé pour le site de démo du thème dont vous ne voudrez pas sur votre site.
{: .notice}

---

## Installation pour un Site Jekyll Existant

1. Clonez les dossiers suivants : `_includes`, `_layouts`, `assets`, et `images`.
2. Clonez les fichiers suivants et personnalisez le contenu : `about.md`, `articles.html`, `index.html`, `tags.html`, `feed.xml`, et `sitemap.xml`.
3. Réglez les variables suivantes dans votre fichier `config.yml` :

{% highlight yaml %}
title:            Titre Site
description:      Description du site pour les metas.
logo:             site-logo.png
disqus_shortname: shortname
search:           true
#Retirer l'url quand vous travaillez localement pour une résolution correcte des urls de base 
url:              http://cequevousvoulez.com

# Information Propriétaire/auteur
owner:
  name:           Vore Nom
  avatar:         votre-photo.jpg
  email:          votre@email.com
  # Liens de silos sociaux utilisés dans le footer. Mettez à jour et retirez à votre guise.
  twitter:
  facebook:
  github:
  linkedin:
  instagram:
  tumblr:
  # Pour la paternité d'auteur Google https://plus.google.com/authorship
  google_plus:    "http://plus.google.com/123123123123132123"

# Les outils d'analytics et de webmaster se placent ici : 
google_analytics:
google_verify:
# https://ssl.bing.com/webmaster/configure/verify/ownership Option 2 content= goes here
bing_verify:

# Liens à exclure dans la barre du haut
# Pour les liens externes ajoutez external: true
links:
  - title: About
    url: /about
  - title: Articles
    url: /articles
  - title: Google
    url: http://google.com
    external: true

# Fuseaux horaires http://en.wikipedia.org/wiki/List_of_tz_database_time_zones
timezone:    America/New_York
pygments:    true
markdown:    kramdown

# https://github.com/mojombo/jekyll/wiki/Permalinks
permalink:   /:categories/:title
{% endhighlight %}

---

## Structure des Dossiers

{% highlight bash %}
so-simple-theme/
├── _includes/
|    ├── browser-upgrade.html  #averstissement mise à jour navigateur < IE8
|    ├── footer.html  #site footer
|    ├── head.html  #site head
|    ├── navigation.html #site navigation and masthead
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
|    |   └── vendor/  #jQuery et Modernizr
|    └── less/
├── images  #images for posts and pages
├── _config.yml  #Jekyll site options
├── about.md  #about page
├── articles.md  #liste tous les posts du plus récent au plus vieux
├── index.html  #page d'accueil. liste les 10 derniers posts
├── tags.html  #liste tous les posts classés par tags
└── sitemap.xml  #sitemap autogenerée pour les moteurs de recherche
{% endhighlight %}

---

## Personnalisation

### _config.yml

La plupart des variables trouvées ici sont utilisées dans les fichiers .html trouvées dans  `_includes` si vous avez besoin d'ajouter ou ôter quoi que ce soit. Un bon endroit pour démarrer serait de modifier les title, tagline, description et url de votre site. Quand vous travaillez localement, mettez en commentaire `url`[^1] ou sinon vous ramasserez un paquet de liens brisés parce qu'ils sont absolus et préfixés avec `{{ "{{ site.url " }}}}` dans les différents `_includes` et `_layouts`. Souvenez vous de dé-commenter `url` au moment de construire pour le déploiement ou de pousser sur votre branche **gh-pages**...

#### Commentaires Disqus 

Créez un compte [Disqus](http://disqus.com) et modifiez `disqus_shortname` dans `_config.yml` vers le  *shortname* Disqus que vous venez d'installer. Pour autoriser le commentaire sur un post, ajoutez ceci au front matter : 

{% highlight yaml %}
comments: true
{% endhighlight %}

#### Information Propriétaire/Auteur

Modifiez votre nom et votre photo d'avatar (200x200 pixels ou plus grande), votre e-mail et vos urls de silos sociaux. Si vous voulez produire un lien vers une image externe sur Gravatar ou quelque chose d'équivalent, vous devrez modifier le chemin dans `head.html` parce qu'il suppose par défaut qu'il est situé dans `/images`.

Ajouter un lien vers votre profil Google+ présente l'avantage d'afficher votre [Paternité d'Auteur Google](https://plus.google.com/authorship) dans les résultats de recherche Google si vous y êtes inscrit.

#### Outils Google Analytics et Webmaster 

Votre ID Google Analytics va ici avec les meta-tags de [Google Webmaster Tools](http://support.google.com/webmasters/bin/answer.py?hl=en&answer=35179) et la vérification de site de  [Bing Webmaster Tools](https://ssl.bing.com/webmaster/configure/verify/ownershi).

#### Liens Navigation en Haut

Modifiez les titres des page/post et les URLs à inclure dans la navigation du site. Pour les liens externes, ajoutez  `external: true`.

{% highlight yaml %}
# échantillon de liens de navigation du haut
links:
  - title: Page À Propos
    url: /about
  - title: Articles
    url: /articles
  - title: Autre Page
    url: /autre-page
  - title: Lien Externe
    url: http://mademistakes.com
    external: true 
{% endhighlight %}

#### Recherche Simple 

Ajouter ce qui suit à  `_config.yml` permet la recherche en utilisant le [plugin Simple Jekyll jQuery](https://github.com/christian-fei/Simple-Jekyll-Search) de  Christian Fei. Cliquez sur chercher déclenchera une surcouche plein-écran qui cherchera les titres de posts utilisant un fichier JSON auto-généré.

{% highlight yaml %}
search: true
{% endhighlight %}

<figure>
  <img src="{{ site.url }}/images/simple-search-screenshot.jpg" alt="search screenshot">
  <figcaption>Cliquer sur chercher déclenche une surcourche qui vous permet de chercher par titre de post.</figcaption>
</figure>

#### Autre trucs

Le reste ne concerne que des réglages habituels de configuration Jekyll. Rien de vraiment fou ici...

### _includes

Pour l'essentiel, vous pouvez les laisser tels quels parce que les détails d'auteur/propriétaire sont extraits de  `_config.yml`. Ceci dit, vous voudrez peut-être personnaliser les mentions de copyright dans `footer.html`.

### Ajouter des Posts et des Pages

Il y a deux layouts pour le contenu principal : `post.html` (pour les posts) et `page.html` (pour les pages). Les deux supportent les grandes **images mises en avant** qui prennent la totalité de la largeur de l'écran, et les deux sont conçus pour des billets de blogs avec beaucoup de texte (ou articles). 

#### Images mises en avant

Une bonne règle pour les vignettes est de conserver les images mises en avant suffisamment belles et larges afin que vous ne poussiez pas le texte trop vers le bas. Une image taillée aux alentours de 1024 x 256 pixels conservera sa taille de fichier réduite avec une résolution acceptable pour la plupart des terminaux. Si vous voulez servir ces images "responsivement", je vous suggére de regarder [Picturefill](https://github.com/scottjehl/picturefill) ou [Adaptive Images](http://adaptive-images.com/).

Les deux layouts supposent que les images mises en avant viventdans le dossier *images*. Pour ajouter une image mise en avant sur un post ou une page, incluez simplement le nom du fichier dans le front matter comme suit : 

{% highlight yaml %}
image:
  feature: feature-image-nomfichier.jpg
  thumb: thumbnail-image.jpg #gardez le carré - 200x200 px c'est bien 
{% endhighlight %}

Si vous voulez mettre en oeuvre l'attribution d'une image mise en avant, utilisez le front matter YAML sur les posts ou pages. Les crédits d'images apparaissent directement sous l'image mise en avant avec un lien retour vers la source originale.

{% highlight yaml %}
image:
  feature: feature-image-filename.jpg
  credit: Michael Rose #nom de la personne ou site que vous souhaitez créditer.
  creditlink: http://mademistakes.com #url vers son site ou la licence
{% endhighlight %}

#### Catégories

Dans le dossier échantillon `_posts` vous pourriez avoir remarqué `category: articles` dans le front matter. J'aime conserver tous les posts groupés dans le même dossier. Si vous décidez de renommer ou d'ajouter des catégories, vous devrez modifier le permalien dans `articles.md` avec le nom du fichier (si renommage).

Par exemple. Disons que vous voulez grouper tous vos posts sous `blog/` au lieu de `articles/`. Dans votre post, ajoutez  `category: blog` au front matter, renommez ou dupliquez `articles.md` en `blog.md` et modifiez le permalien dans ce fichier en `permalink: /blog/index.html`.

Si vous faites ça correctement,  `/blog` devrait être une page listant tous les posts du site.

#### Vignettes Post/Page pour OG et Twitter Cards

Les vignettes de posts et pages fonctionnent de la même façon. Celles-ci sont utilisées par les méta-tags [Open Graph](https://developers.facebook.com/docs/opengraph/) et [Twitter Cards](https://dev.twitter.com/docs/cards) trouvés dans `head.html`. Si vous n'assignez pas un thumbnail, l'image que vous avez assignée à `site.owner.avatar` dans `_config.yml sera utilisée.

Voici un exemple de ce à quoi pourrait ressembler un tweet vers votre site si vous activez Twitter Cards et incluez tous les métas dans votre YAML de post.

![Twitter Card summary large image screenshot]({{ site.url }}/images/twitter-card-summary-large-image.jpg)

#### Vidéos

Les embarquements de vidéos sont responsive et passent à l'échelle avec la largeur du bloc de contenu principal à l'aide de [FitVids](http://fitvidsjs.com/).

Pas certain si ceci impacte seulement Kramdown ou si c'est un problème avec Markdown en général. Mais l'ajout d'embeds vidéo YouTube provoque des erreurs à la construction de votre site Jekyll. Pour pallier ça, ajoutez un espace entre les balises `<iframe>` et retirez  `allowfullscreen`. Exemple en-dessous :

{% highlight html %}
<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>
{% endhighlight %}

#### Twitter Cards

Twitter cards permet d'attacher des images et résumés de posts aux Tweets qui font un lien vers votre contenu. Les meta-tags de Summary Card ont été ajoutés à `head.html` pour supporter cela, vous devez juste  [valider et mettre en oeuvre votre domaine](https://dev.twitter.com/docs/cards) pour l'activer.

#### Link Post Type

Simple Theme supporte désormais les **link posts**, popularisés par John Gruber. Pour les activer ajoutez simplement  `link: http://url-que-vous-voulez-lier` au front matter YAML du post et c'est fini. Voici un  [exemple  de post de lien]({{ site.url }}/articles/sample-link-post) si vous avez besoin d'un visuel.

---
<span id="theme-development"> </span>  


## Développement du Thème

Si vous voulez skinner facilement les couleurs et fontes des thèmes, jetez un oeil sur `variables.less` dans `assets/less/` et faites les modifications nécessaires pour modifier les variables de couleurs et de fontes. Pour rendre le développement plus facile, j'ai installé un script de build Grunt pour compiler/minifier les fichiers LESS à l'intérieur de `main.min.css` et lint/concatenate/minify tous les scripts à l'intérieur de `scripts.min.js`. [Installez Node.js](http://nodejs.org/), puis [installez Grunt](http://gruntjs.com/getting-started), et pour finir installez les dépendances pour le thème contenues dans `package.json`:

{% highlight bash %}
npm install
{% endhighlight %}

À partir de la racine du thème, utilisez `grunt` pour reconstruire le CSS, concaténer les fichiers JavaScript, et optimiser les fichiers .jpg, .png, et .svg files dans le répertoire `images/`. Vous pouvez aussi utiliser `grunt watch` en combinaison avec `jekyll build --watch` pour regarder les mises à jours de vos fichiers LESS et JS files que Grunt reconstruira automatiquement ensuite au fur et à mesure que vous écrivez du code qui à son tour auto-générera votre site Jekyll quand vous travaillez localement.

Et si la ligne de commende n'est pas votre truc (vous utilisez Jekyll, aussi il est probable que ce le soit), [CodeKit](http://incident57.com/codekit/) pour Mac OS X et [Prepros](http://alphapixels.com/prepros/) pour  Windows sont de belles alternatives.

---

## Questions ?

Vous avez un problème à faire fonctionner quelque chose ou vous voulez savoir pourquoi j'ai installé quelque chose d'une certaine façon ? Pinguez-moi sur Twitter [@mmistakes](http://twitter.com/mmistakes) ou [soumettez un problème GitHub](https://github.com/mmistakes/so-simple-theme/issues/new).

## Licence

Ce thème est libre et c'est du logiciel open source, distribué sous la [Licence GNU General Public]({{ site.url }}/LICENSE) version 2 ou plus. Sentez-vous donc libre d'utiliser ce thème Jekyll sur votre site sans faire de lien arrière ou toute utilisation de divulgation.

Si vous voulez créditer l'auteur sur votre blog ou lui tweeter un message [@mmistakes](https://twitter.com/mmistakes), ce serait vraiment charmant ! 

[^1]: utilisé pour générer les urls absolues dans *sitemap.xml*, *feed.xml*, et pour les urls canoniques dans *head.html*. N'ajoutez pas de `/` après dans votre url de base par ex : http://mademistakes.com. Quand vous développez localement, retirez ou dé-commenter cette ligne afin d'utiliser les assets CSS, JS, et image locaux.