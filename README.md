# DECAF Blog

👉 [https://blog.decaf.de](https://blog.decaf.de)


## How to set up and run Jekyll on your machine

__For setup instructions, see [SETUP.md](SETUP.md)!__

Start your blog with:

    $ bundle exec jekyll serve

To preview your site with [drafts](https://jekyllrb.com/docs/posts/#drafts) and future posts and unpublished posts, run Jekyll with all those switches (see [docs](https://jekyllrb.com/docs/configuration/options/#build-command-options)):

    $ bundle exec jekyll serve --drafts --future --unpublished


## How to blog

The `_posts` folder is where your blog [posts](https://jekyllrb.com/docs/posts/) live. You typically write posts in Markdown, HTML is also supported.

All blog post files must begin with [front matter](https://jekyllrb.com/docs/front-matter/) which is used to set a layout and other meta data, for example:

```
---
layout: post
title: "Jobs: Laravel in Berlin, Westfalen oder remote"
author: ds

description: "Wie cool wäre es, wenn du genau die richtige Person bist und das hier liest!"
image: /content/images/2019/02/laravel_01.png
imageClass: seamless
featured: true
more: true
---
```

Front matter details:

| Options       | Description                        | Required |
|---------------|------------------------------------|----------|
| `layout`      | The page layout. It’s usually `post`, but sometimes you want to use a variant:<br>`post-short`: For short posts. Does not show post title, uses big typo. | Yes |
| `title`       | The post title. | Yes |
| `author`      | The post author. Has to match with an `id` from `_data/authors.yml`. | Yes |
| `description` | A post description. Should be no longer than 160 chars. Will be used in several contexts, like post excerpts or page meta data for social media. | |
| `image`       | A post image URL. Like description, the image will be used in several contexts. | |
| `imageClass`  | `seamless`, if the image should not have a white outline. You probably want transparent images to be seamless. | |
| `featured`    | `true`, if you like the post get listed on the »Featured Posts« page.<br>_Hint: Excerpt makes use of `description` and `image`, if available!_ | |
| `more`        | `true`, if you like to show an excerpt only and have a »Read more« button that links to the post. Typically used on long blog posts.<br>_Hint: Excerpt makes use of `description` and `image`, if available!_ | |


## How to publish

Just commit and push. Wait ~1 min and see it live! `\o/`


## What else?

### Twitter posts

We re-publish a lot of Tweets on our blog. In order to make Jekyll recognize a Twitter post, just use the __tweet’s Id for the post slug__, like `YEAR-MONTH-DAY-ID.md`.

Twitter posts don’t show the post title, use big typo (since tweets are short) and they provide a link to the tweet on Twitter.

### Images

Drop your images in the `content/images/` folder and refer to them by relative URLs, for example:

```
![Pic of a cat](/content/images/2019/03/cat.jpg)
```

If your image is transparent, you probably want to __avoid the default white outline__. In this case, switch to HTML notation and add a class `seamless` to the image:

```html
<img class="seamless" src="/content/images/2019/03/cat.jpg" alt="Pic of a cat">
```

### Code with syntax highlighting

We make use of [Prism JS](https://prismjs.com) for code highlighting. You can create fenced code blocks by placing triple backticks before and after the code block, as you know it from [GitHub Flavored Markdown](https://help.github.com/en/articles/creating-and-highlighting-code-blocks). An optional language identifier enables syntax highlighting.

However, this is special to Jekyll: __if your code snippet contains curly braces__, you will likely need to place `{% raw %}` and `{% endraw %}` tags around your code! (See [Liquid docs](https://shopify.github.io/liquid/tags/raw/) for raw.)

### Lazy loading

Images from `content/images/` will be lazy loaded per default. If you want iframes to lazy load as well, just change their `src` to `data-lazy-src`, like

```html
<iframe data-lazy-src="https://giphy.com/embed/22nMX60cwdx5K" ... ></iframe>
```
