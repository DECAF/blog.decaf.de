---
layout: post
title: "‘Why BEM?’ in a nutshell"
featured: true
image: "/content/images/2015/06/bem2.png"
date: '2015-06-24 15:34:15'
tags:
- css
- bem
- web-components
---

_(Update ~~2018~~ 2019: this stuff is still relevant if you’re not writing CSS-in-JS!)_

<img style="width: 15%; outline: none;" src="/content/images/2015/06/bem2.png" alt="BEM">

The two base concepts of CSS? Inheritance and specificity.

Apart from the benefits: what’s so bad about it? Well, CSS’ __inheritance__ is infinite. There’s no function scope or closure like in programming. Styles you fill in on top will flow down and will never reach a bottom. When you write CSS, there is _always_ context and you’re about to touch it!

What’s so bad about __specificity__? You need to become _more_ specific to win over existent specificity. It’s `!important` to be clear on this feature.

##### Modularity?

Today’s web development is driven by the purpose of modularity: chop projects into pieces to make it manageable. We build upon APIs, allow for separation of concerns and keep stuff simple and stupid.

Of course we are willing to write modular CSS, too. But its base features inheritance and specificity do not play nice with modular concepts. Think of modules containing modules containing modules… — Inheritance is hard to handle (at least for humans!) and we’re missing scope.

##### Web components!

Web Components will hopefully provide some CSS scope (see [Shadow DOM](http://webcomponents.org/articles/introduction-to-shadow-dom/)). But while waiting for Web Components to get finished and implemented in common browsers, we’d better use some proper _workarounds_ like:

<img style="width: 30%; outline: none;" src="/content/images/2015/06/bem.png" alt="BEM">

### BEM.

Why use [BEM](https://bem.info)? Because it tries to get the best out of today’s CSS concerning modularity:

+ Avoids inheritance and provides some sort of __scope__ by using _unique_ CSS classes per element (like `.my-component__list-item`).
+ Reduces style conflicts by keeping CSS __specificity__ to a minimum level.

This is what BEM is all about.

---

<blockquote class="twitter-tweet" data-cards="hidden" lang="de"><p lang="en" dir="ltr"><a href="https://twitter.com/hashtag/BEM?src=hash">#BEM</a> is all about low level CSS specificity and sort of scope by means of unique CSS classes per element.&#10;&#10;<a href="http://t.co/jEa9JcemcE">http://t.co/jEa9JcemcE</a> <a href="https://twitter.com/hashtag/b_?src=hash">#b_</a></p>&mdash; DECAF (@_DECAF) <a href="https://twitter.com/_DECAF/status/614154928878186497">25. Juni 2015</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

---

## — But wait!

> My HTML looks all bloated and messy with BEM!

_This seems to be the most frequently mentioned argument against BEM._

Remember, until CSS supports scope, __there is no way to get around inheritance__ in modular environments other than sticking _unique_ CSS classes (or attributes) to any given element. Whenever you apply styles by element type selectors (like `p` or `li`) or generic classes (like `.title` or `.active`) you apply styles not only to the element itself but to a whole _cascading_ context. Even if the context doesn’t exist yet, it may be expanded until someone adds another module or component to your HTML.
— Think of modularity as _any_ module may contain further modules!

So, _bloated_ HTML with BEM? Y’d better call it functional!
And it will be gzipped anyway.

> Why not use element type selectors with child or sibling combinators (like `ul > li + li`) to avoid inheritance issues?

Nested selectors raise CSS specificity. You need to become _more_ specific to win over existent specificity. __Modular contexts require low specificity!__

(Furthermore, your CSS would be sort of tight coupled with the HTML. Better get loose coupled and apply styles by unique CSS classes not element structure.)

> Nesting is such a brilliant feature of pre-processors! With BEM it sucks.

With BEM _any_ element (more precisely: any group of elements of the same type) can be selected by its _unique_ class. You don’t need selector nesting, even in pre-processors.

That said, [Sass 3.3 supports BEM-style nesting](http://mikefowler.me/2013/10/17/support-for-bem-modules-sass-3.3/)!

---

##### Comments?

We’d love to get your feedback on twitter: [@_DECAF](https://twitter.com/_DECAF).
And did you know: hashtag for BEM is [#b\_](https://twitter.com/search?q=%23b_).
