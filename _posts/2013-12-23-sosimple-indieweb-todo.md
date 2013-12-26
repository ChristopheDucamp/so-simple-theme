---
layout: post
title: Bricolage IndieWeb pour la localisation de So Simple
description: "Plan de route 2014 : dates, recherche et blocs de construction indieweb."
modified: 2013-12-26 08:05
category: articles
tags: [todo indieweb localisation]
image:
  feature: so-simple-sample-image-1.jpg
  credit: Michael Rose
  creditlink: http://mademistakes.com
comments: true  
---

## Étude de localisation : localiser les dates, la recherche sans oublier... les briques de base indieweb 

Après un début du mois difficile pour ébaucher une [page personnelle basique hébergée sur GitHub](http://cyberhippie.fr/news/2013/12/03/premier-pas-sur-jekyll/) et l'étude d'un  [tutoriel de cuisine pour créer un projet sur GitHub](http://cyberhippie.fr/news/2013/12/21/demarrer-avec-pages-github/), quelques réjouissances sont attendues pour explorer  **quelques jolis thèmes Jekyll**. 

Toujours beaucoup de difficultés à comprendre les subtilités de Git à ligne de commande, les assemblages de briques étranges et pré-processeurs m'ouvrent un tout nouveau monde plein de perspectives pour avancer sur l'indieweb.

L'intention de ce post : garder un mémo des **futurs trucs à faire** durant les vacances. Je rêverais que la structure du thème **So Simple** développé par <span class="h-card">[Michael](http://mademistakes.com/about/)</span> (SlashGen à NYC) soit plus un peu plus *indieweb-friendly*. 

Premier ressenti à cette heure : la phase 1 [IndieMark](http://indiewebcamp.com/IndieMark) me semble jouable pour un livrable début 2014. 

Après avoir démarré la localisation de quelques dates sur les pages de structure (index, articles et tags), deux sections restent à creuser. 

### 1.  Moteur de recherche 
Précédemment fonctionnel, il ne semble plus vouloir démarrer ce matin. 
Solution : Réinstaller une instance fraîche du thème avant étude des termes à traduire.

### 2. blocs de construction indieweb

<<<<<<< HEAD
Une [check-list des blocs de construction](http://indiewebcamp.com/building-blocks-fr) sera complétée point par point. Pour cette section d'enrichissement sémantique, l'inspiration sera à dénicher sur les instances de mes quelques [collègues indieweb ayant choisi d'avancer Jekyll](http://indiewebcamp.com/Jekyll) 
=======
{% highlight html %}
{% raw %}
<time class="dt-published" datetime="{{ post.date | date_to_xmlschema }}">{{ post.date | date: "%Y-%m-%d" }}</time>
{% endraw %}
{% endhighlight %}

Statut : [Recherche personnelle en cours - attente de raffinage](http://christopheducamp.github.io/news/2013/12/26/jekyll-localiser-la-date/) 

### 2.  Moteur de recherche 

Le moteur de recherche  fonctionne parfaitement en local mais pas en ligne. 
Par ailleurs, quelques termes simples sont à traduire lors de l'utilisation du moteur de recherche de titres (Chercher, ...). 

### 3. blocs de construction indieweb

Une [check-list des blocs de construction](http://indiewebcamp.com/building-blocks-fr) sera à compléter point par point. Pour cette section, je prévois d'aller chercher quelque inspiration sur les instances de quelques [collègues indieweb ayant choisi d'avancer Jekyll](http://indiewebcamp.com/Jekyll) 
>>>>>>> 32cfb853ae0dc583d216a36fb557797ad08d6c40

Vos commentaires, idées, suggestions et/ou *fork* + *pull-request* du fichier index.html sont bienvenus.

ChronoRêve de vacances : évaluer ce thème "photo" avec quelques visuels personnels de deux grosses *machines de destruction* évoluant sous mes fenêtres...

Bonnes fêtes de fin d'année et à plus tard.

## Ailleurs 
<span class="u-syndication">[conversation sur twitter](https://twitter.com/xtof_fr/status/415266536840904704)</span>
