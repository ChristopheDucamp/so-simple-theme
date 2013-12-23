---
layout: post
title: "Un Post avec des Images"
description: "Exemples et code pour afficher des images dans les posts."
category: articles
tags: [post echantillon, images, test]
comments: true  
---

Voici quelques exemples de ce à quoi peut ressembler un post avec des images. Si vous désirez afficher deux ou trois images côte à côte de manière responsive, utilisez `figure` avec la `class`e appropriée. 
Chaque instance de `figure` est auto-numérotée et affichée dans la légende.

## Figures (pour images ou vidéo)

### One Up

<figure>
	<a href="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_b.jpg"><img src="http://farm9.staticflickr.com/8426/7758832526_cc8f681e48_c.jpg"></a>
	<figcaption><a href="http://www.flickr.com/photos/80901381@N04/7758832526/" title="Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr">Morning Fog Emerging From Trees by A Guy Taking Pictures, on Flickr</a>.</figcaption>
</figure>

### Two Up

Appliquez la classe `half` comme ceci afin d'afficher deux images côte à côte qui partagent la même légende.

{% highlight html %}
<figure class="half">
	<img src="/images/image-filename-1.jpg">
	<img src="/images/image-filename-2.jpg">
	<figcaption>Légende décrivant ces deux images.</figcaption>
</figure>
{% endhighlight %}

Et vous obtiendrez quelque chose qui ressemble à cela : 

<figure class="half">
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<img src="http://placehold.it/600x300.jpg">
	<img src="http://placehold.it/600x300.jpg">
	<figcaption>Deux images.</figcaption>
</figure>

### Three Up

Appliquez la classe `third` comme ceci pour afficher trois images côte à côte qui partagent la même légende.

{% highlight html %}
<figure class="third">
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<figcaption>CapLégende décrivant ces trois images.</figcaption>
</figure>
{% endhighlight %}

Et vous obtiendrez quelque chose qui ressemble à cela : 

<figure class="third">
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<a href="http://placehold.it/1200x600.jpg"><img src="http://placehold.it/600x300.jpg"></a>
	<figcaption>Trois images.</figcaption>
</figure>