---
layout: post
title: Post de Coloration Syntaxique
description: "Post de démonstration affichant les différentes façons de colorer le code dans Markdown."
category: articles
tags: [post échantillon, code, enluminure, éclairage]
image:
  feature: so-simple-sample-image-5.jpg
  credit: Michael Rose
  creditlink: http://mademistakes.com
comments: true  
---

La coloration syntaxique est une fonctionnalité qui affiche le code source, en différentes couleurs et fontes selon la catégorie des termes. Cette fonctionnalité facilite l'écriture dans un langage structuré comme un langage de programmation ou un langage de marquage parce que les erreurs de structures et de syntaxes sont visuellement distinctes. Colorer et enluminer le code n'impactent pas le sens du texte lui-même ; ceci est uniquement conçu pour les lecteurs humains.[^1]

[^1]: <http://en.wikipedia.org/wiki/Syntax_highlighting>

### Blocs de Code Pygments

Pour modifier le style et mettre en valeur les couleurs éditez  `/assets/less/pygments.less` et compilez  `main.less` avec votre pré-processeur favori. Ou éditez `main.css` si c'est votre truc, les classes que vous voulez modifier commencent toutes par `.highlight`.

{% highlight css %}
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
{% endhighlight %}

{% highlight html %}
{% raw %}
<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Article précédent</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Article suivant</a>
    {% endif %}
</nav><!-- /.pagination -->
{% endraw %}
{% endhighlight %}

{% highlight ruby %}
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagged: '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "An archive of posts tagged #{tag}."
    end
  end
end
{% endhighlight %}


### Bloc de Code Standard 

    {% raw %}
    <nav class="pagination" role="navigation">
        {% if page.previous %}
            <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Article précédent</a>
        {% endif %}
        {% if page.next %}
            <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Article suivant</a>
        {% endif %}
    </nav><!-- /.pagination -->
    {% endraw %}


### Blocs de Code Fenced

Pour modifier le style et mettre en avant les couleurs, éditez `/assets/less/coderay.less` et compilez `main.less` avec votre pré-processeur favori. Ou éditez `main.css` si c'est votre truc, les classes que vous voulez modifier commencent toutes par `.coderay`. Les numéros de ligne et quelques autres trucs peuvent être modfiés dans  `_config.yml` sous `coderay`.

~~~ css
#container {
    float: left;
    margin: 0 -240px 0 0;
    width: 100%;
}
~~~

~~~ html
{% raw %}<nav class="pagination" role="navigation">
    {% if page.previous %}
        <a href="{{ site.url }}{{ page.previous.url }}" class="btn" title="{{ page.previous.title }}">Article précédent</a>
    {% endif %}
    {% if page.next %}
        <a href="{{ site.url }}{{ page.next.url }}" class="btn" title="{{ page.next.title }}">Article suivant</a>
    {% endif %}
</nav><!-- /.pagination -->{% endraw %}
~~~

~~~ ruby
module Jekyll
  class TagIndex < Page
    def initialize(site, base, dir, tag)
      @site = site
      @base = base
      @dir = dir
      @name = 'index.html'
      self.process(@name)
      self.read_yaml(File.join(base, '_layouts'), 'tag_index.html')
      self.data['tag'] = tag
      tag_title_prefix = site.config['tag_title_prefix'] || 'Tagués : '
      tag_title_suffix = site.config['tag_title_suffix'] || '&#8211;'
      self.data['title'] = "#{tag_title_prefix}#{tag}"
      self.data['description'] = "Une archive des posts tagués #{tag}."
    end
  end
end
~~~