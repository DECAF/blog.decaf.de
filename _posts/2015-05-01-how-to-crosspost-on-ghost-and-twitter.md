---
layout: post
title: How to crosspost on Ghost and Twitter
image: "/content/images/2015/05/twitter-ghost_01.png"
date: '2015-05-01 16:39:00'
tags:
- tryghost
---

We do not publish long posts that often. We're better off with short posts, and that is why we implemented some _crossposting feature_ for sharing thoughts both on the blog (Ghost) and on [Twitter](https://twitter.com/_DECAF/).

It's a pretty easy manual workflow we're talking about:
<br>

### Step 1: Use Twitter status ID for Post URL

![Screenshot 1](/content/images/2015/05/twitter-ghost_01.png)

Ghost doesn't allow for custom fields to date, but using the Post URL feels fine for us. Your blog post will have a URL similar to the correspondent Twitter status (Tweet).
<br>

### Step 2: Copy, paste, add sugar.

![Screenshot 2](/content/images/2015/05/twitter-ghost_02.png)

Paste in your text and media. Add some markdown flavour if you like to, e.g. for links or text formatting you cannot use in a tweet.

When dealing with short posts, we don't show up with an excerpt but the full post straightaway. Obviously, there's no need for a post title as Twitter doesn't have titles, too.
However, _blog posts_ do have post titles and you will strike them in the RSS feed, in the sitemap and inside of search results. That is why we need brave post titles; even for our short posts.

Finally, tag the post with `twitter` and it will feel like a tweet immediately.
<br>

### Step 3: Adjust your Ghost theme

Casper theme solution: hook your _special post_ conditional code right into the loop (`partials/loop.bhs`):

{% highlight handlebars %}{% raw %}
{{#foreach posts}}

	{{#has tag="Twitter"}}

        <article class="{{post_class}}">
            <section class="post-content">
                <p>{{content}}</p>
            </section>
            <footer class="post-meta">
				{{#if author.image}}<img class="author-thumb" src="{{author.image}}" alt="Author image" nopin="nopin"/>{{/if}}
				{{author}}
				{{tags prefix=" on "}}
                <time class="post-date" datetime="{{date format='YYYY-MM-DD'}}"><a
                    href="https://twitter.com/_DECAF/status/{{slug}}">{{date format="DD MMMM YYYY"}}</a></time>
                <a class="post-link" href="{{url}}">Link</a>
            </footer>
        </article>

	{{else}}

        …
{% endraw %}{% endhighlight %}

Have a look at the slug: we've hardcoded the URL to our Twitter account in there.
<br>

### Step 4: Add style.

You may like to increase the font size:

{% highlight css %}{% raw %}
.post.tag-twitter {
  	font-size: 1.3em;
  	line-height: 1.5;
}
{% endraw %}{% endhighlight %}
<br>

### Result

![Screenshot 3](/content/images/2015/05/twitter-ghost_03.png)

¯\\\_(ツ)_/¯
