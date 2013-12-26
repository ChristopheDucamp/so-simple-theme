---
layout: post
title: Bricolage IndieWeb pour la localisation de So Simple
description: "Plan de route 2014 : dates, recherche et blocs de construction indieweb."
modified: 2013-12-23
category: articles
tags: [todo indieweb localisation]
image:
  feature: so-simple-sample-image-1.jpg
  credit: Michael Rose
  creditlink: http://mademistakes.com
comments: true  
---

## Étude de localisation : localiser les dates, la recherche sans oublier... les briques de base indieweb 

Après la construction au début du mois d'une [page personnelle basique hébergée sur GitHub](http://cyberhippie.fr/news/2013/12/03/premier-pas-sur-jekyll/),  l'étude de ce  [tutoriel pour créer une première page projet sur GitHub](http://cyberhippie.fr/news/2013/12/21/demarrer-avec-pages-github/), 
j'ai la tête qui chauffe ce soir après une plongée difficile dans la structure de **quelques jolis thèmes Jekyll**. 

Toujours non programmeur, la récente découverte de Git à ligne de commande, les assemblages de trucs étranges comme l'usage de pré-processeurs m'ouvrent un tout nouveau monde plein de perspectives pour avancer sur l'indieweb.

L'intention de ce post : garder un mémo des **trucs à faire** durant les vacances. Je rêverais que la structure du thème **So Simple** développé par <span class="h-card">[Michael](http://mademistakes.com/about/)</span> (SlashGen à NYC) soit plus un peu plus *indieweb-friendly*. 

Premier ressenti à cette heure : la phase 1 [IndieMark](http://indiewebcamp.com/IndieMark) me semble jouable pour un livrable début 2014. 

Trois sections restent ouvertes pour les vacances  de Noël : 

### 1. [variables jekyll](http://jekyllrb.com/docs/variables/) de dates à localiser en français + format ISO 8601

Tout en respectant le format de représentation [iso 8601](http://microformats.org/wiki/iso-8601-fr), l'idée serait d'afficher simplement des variables de dates à un format plus lisible pour les humains comme  **jour mois année**.  Par exemple, la date du jour sur ce fuseau horaire est le *lundi 23 décembre 2013*. Exemple pour la ligne de code figurant sur le fichier `index.html` restant à retravailler à cette heure : 

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

Vos commentaires, idées, suggestions et/ou *fork* + *pull-request* du fichier index.html sont bienvenus.

ChronoRêve de vacances : évaluer ce thème "photo" avec quelques visuels personnels de très grosses machines de chantier évoluant de l'autre côté de la rue.

Bonnes fêtes à tous et à plus tard.

## Ailleurs 
<span class="u-syndication">[conversation sur twitter](https://twitter.com/xtof_fr/status/415266536840904704)</span>
