---
layout: post
title: Ghost 0.7.2 with public API
description:
author: ds
---

The Ghost folks recently published [0.7.2](http://dev.ghost.org/ghost-0-7-2/) including public API features. They’re still in beta which is why you have to activate them in the labs section of your Ghost admin.

> For those who've been waiting for the {% raw %}`{{#get}}`{% endraw %} helper, this release is your first chance to start playing with it.

Indeed we like to play with it. Since this blog has switched from [WordPress to Ghost](http://blog.decaf.de/2015/02/23/look-ma-new-blog/) in February, I was about to add some archives and tag list pages. But without plugins (called _apps_ in the ghost universe) and API there hasn’t been a proper chance to implement these kind of pages.  

Now it is. Find them using the menu button top right!

![Look, new navigation and content pages!](/content/images/2015/12/decaf-blog-public-api.jpg)

----

## Okay, how to use the {% raw %}`{{get}}`{% endraw %} helper?

First up, check out the full [get helper documentation](http://themes.ghost.org/docs/get).

This is the complete relevant source for our __archives page__:

{% highlight handlebars %}{% raw %}
{{#get "posts" order="published_at desc" limit="all" include="author,tags" as |articles pages|}}

  <ul class="archive-list">

    {{#foreach articles}}

      <li class="archive-list__item">

        <article class="post">
          <header class="post-header">
            <h2 class="post-title"><a href="{{url}}">{{{title}}}</a></h2>
          </header>
          <footer class="post-meta">
            {{#if author.image}}<a href="{{@blog.url}}/author/{{author.slug}}"><img class="author-thumb" src="{{author.image}}" alt="{{author.name}}" nopin="nopin"/></a>{{/if}}
            {{author}}
            {{tags prefix=" on "}}
            <time class="post-date" datetime="{{date format='YYYY-MM-DD'}}">{{date format="DD MMMM YYYY"}}</time>
          </footer>
        </article>

      </li>

    {{/foreach}}

  </ul>

  <p>{{pages.total}} Posts</p>

{{/get}}
{% endraw %}{% endhighlight %}

Query for the __tags page__:

{% highlight handlebars %}{% raw %}
{{#get "tags" limit="all" include="count.posts" order="count.posts desc"}}
{% endraw %}{% endhighlight %}

Query for the __about page__ including author list:

{% highlight handlebars %}{% raw %}
{{#get "users" limit="all" include="count.posts" order="count.posts desc"}}
{% endraw %}{% endhighlight %}

Query for __featured posts__:

{% highlight handlebars %}{% raw %}
{{#get "posts" order="published_at desc" limit="all" include="author,tags" filter="featured:true" as |articles|}}
{% endraw %}{% endhighlight %}

Thank you, Ghost dev team!
