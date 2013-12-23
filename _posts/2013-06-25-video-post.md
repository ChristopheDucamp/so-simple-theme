---
layout: post
title: "Un Post Avec une Vidéo"
description: "Les descriptions personnalisées écrites de posts sont la façon de faire ... si vous n'êtes pas trop paresseux."
category: articles
tags: [post echantillon, video]
comments: true
---

<iframe width="560" height="315" src="http://www.youtube.com/embed/SqYiglufb8Y" frameborder="0"> </iframe>

Les embarquements vidéo sont responsive et passent à l'échelle avec la largeur du bloc de contenu principal grâce à l'aide de [FitVids](http://fitvidsjs.com/).

Pas certain si ceci n'impacte que Kramdown ou si c'est un problème avec Markdown en général. Mais ajouter des embeds vidéo YouTube provoque des erreurs au moment de construire un site Jekyll. Pour pallier ça, ajoutez un espace entre les balises `<iframe>` et retirez `allowfullscreen`. Exemple en-dessous :

{% highlight html %}
<iframe width="560" height="315" src="http://www.youtube.com/embed/PWf4WUoMXwg" frameborder="0"> </iframe>
{% endhighlight %}