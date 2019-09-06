---
layout: post
title: 'Introducing Gremlin.js: web components for websites, not apps.'
description: How to use Gremlin.js with HTML Custom Elements and BEM CSS to build modular server-side driven websites, not web apps.
image: /content/images/2015/12/gremlinjs.png
imageClass: seamless
author: aw
featured: true
---

__Summary: How to use [Gremlin.js](http://grml.in) with HTML [Custom Elements](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Custom_Elements) and [BEM](https://en.bem.info) CSS to build modular server-side driven websites, not web apps.__

<img class="seamless" style="max-width: 150px;" src="/content/images/2015/12/gremlinjs.png" alt="Fluffy thing in a wooden box">
-----

[We](http://decaf.de) build websites. The ones where you click a link and the page gets redirected. Where the bigger part of HTML comes up generated __server-side__, not client-side. While we like to build web apps, most of the time we have to deal with some CMS or shopping system that does not allow us to develop anything app-like in a reasonable amount of time.

We love our modern frontend though. ES6, CSS ~~pre~~ post processors, highly complex build systems with Gulp and whatnot. I can’t live without that anymore. And I don’t want to write my JavaScript like 5 years ago, when we assembled some single `main.js` full of jQuery plugin spaghetti code. I want to profit from all the recent additions to the browsers toolbelt!

## Modularize your website!

Websites contain a lot of modules, aka components. Big ones like an image gallery or a slider, smaller pieces like a button. __Components will be nested__, of course, and they should not depend on anything but themselves. 

If you build self-contained components, things will be isolated, they will work everywhere. You take and throw them into another (modularized) project and you’re done. Furthermore, the code will be much more manageable if you work in a team. Everybody knows where to look at, because the component tells you by its name. And if you use a package manager like bower or npm you may even want to put some of your components into separate packages. You can reuse them in other projects easily this way.

Having said this: everything gets better if you build a website with modular, reusable and small pieces.

But while the paradigm of modular code is quite obvious to follow when writing JavaScript, PHP, Ruby or stuff, it’s not that evident __how to build modular HTML and CSS__. With HTML and CSS there is no scope. Your HTML may collide with existing structure and your CSS may blow up the whole thing if you mess around with inheritance and specificity.

_(Remember humans aren’t good in measuring inheritance and spotting conflicts. However, browsers are pretty tough. They know code.)_

Well. How to write modular HTML and CSS?

### Use Web Components.

I would love to, but sadly [this is not an option yet](http://jonrimmer.github.io/are-we-componentized-yet/). Web Components will be the way to go for me once they are supported by all the browsers I have to consider. But until then, we need to find a proper workaround.

![Panda oh no](https://i.giphy.com/14aUO0Mf7dWDXW.gif)

<small>Source: [giphy](https://gph.is/19lfu4P)</small>

----

## Step 1: use BEM for your CSS

> When you write CSS, there is always context and you’re about to touch it!  
> <small>[‘Why BEM?’ in a nutshell](http://blog.decaf.de/2015/06/24/why-bem-in-a-nutshell/)</small>

As long as __CSS does not provide scope__, we think [BEM](https://en.bem.info) is the best workaround we have. With BEM you avoid styling based on element type selectors (like `p` or `li`) or generic classes (like `.title` or `.active`). You apply styles by _unique_ (as in unique by type) CSS classes instead and thereby archive some sort of pseudo scope. It’s no real scope at all, but you don’t interfere with other element styles and avoid inheritance issues — it _feels_ like scope.

Short version: With BEM you write today’s most modular CSS.

<blockquote class="twitter-tweet" lang="de"><p lang="en" dir="ltr">Again: why use BEM for CSS?&#10;—Because you won’t be able to write modular CSS without. <a href="https://twitter.com/hashtag/b_?src=hash">#b_</a></p>&mdash; DECAF (@_DECAF) <a href="https://twitter.com/_DECAF/status/672332364828303360">3. Dezember 2015</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

## Step 2: add your very own HTML tags

One of the things Web Components use in the background are [Custom Elements](https://developer.mozilla.org/en-US/docs/Web/Web_Components/Custom_Elements). Custom Elements allow the developer to create their very own HTML elements, describing the elements functionality with JavaScript.
The native browser support [is pretty poor](http://caniuse.com/#feat=custom-elements) today, but there are multiple libraries providing __polyfills__ for the old browsers we all love so much.

A Custom Element is created by calling `document.registerElement()`:

```javascript
var Gallery = document.registerElement('photo-gallery');
```

You then use it in your HTML:

```markup	
<photo-gallery>
  <!-- photo gallery html !-->
</photo-gallery>
```

or create new elements with JavaScript:

```javascript
document.body.appendChild(new Gallery());
```

_(This post is not meant to be a tutorial on custom elements, though. Plenty of articles about custom elements can be found, for example at [htm5rocks](http://www.html5rocks.com/en/tutorials/webcomponents/customelements/).)_

Using the native API is a little bit cumbersome, of course. It’s one of the things I don’t want to deal with in my daily work.  

__That’s why I built Gremlin.js.__

-----

# Introducing [Gremlin.js](http://grml.in)

<img class="seamless" style="max-width: 400px;" src="/content/images/2015/12/gremlinjs.png" alt="Fluffy thing in a wooden box">

Gremlin.js is a library for 

> dead simple web components

My problem with existing libraries was (and still is) that they tend to be highly complex, have a huge footprint, and — most importantly — __don’t like the server-side rendering approach__ too much.   

I needed something that would allow me to build components with Custom Elements for _normal websites_ and started to build the first version of Gremlin.js some years ago.

Basically I wanted it to:

* __observe the DOM__, looking for new elements. No matter if it’s available on page load or added later dynamically (see [__watched.js__](https://github.com/grmlin/watched)).
* __instantiate a Gremlin class__ for every component once it’s found in the DOM. 
* make it easily extensible via __plugins__.
* use __server-side__ rendered HTML for components.

This worked pretty good and I used it in a lot of projects. Sadly, the markup wasn’t that great as I had to rely on extra attributes to find and create the components:

```markup
<div data-gremlin-name="HelloWorld"></div>
```

All this changed when I taught Gremlin.js to use __Custom Elements__. 

### Custom element gremlins!

You can use any HTML you like for new elements, as long as it fulfills [the browser's constraints](http://grml.in/learn/#tag-names) for custom elements.

```markup
<hello-world>
  <button>tap me please!</button>
</hello-world>
```

You can render the components content on the server, or, if you like, use a JS template engine to do so when the component is instantiated.

To make the component alive, we create a new gremlin with `gremlins.create`. It uses the native `document.registerElement` in the background and registers the new element in the current document.

```javascript
const gremlins = require('gremlins');

gremlins.create('hello-world', {
  initialize: function(){
    let button = this.el.querySelector('button');
    button.addEventListener('click', () => alert('hello world!'));
  }
});
```

Gremlin.js offers the most important parts to build a component:

**Spec:**  

* `initialize`  
constructor called for every instance of this element found in and added to the DOM
* `destroy`  
destructor called if an element is removed from the DOM
* `attributeDidChange`  
callback if an attribute of the DOM element changed

**Component instance:**  

* `this.el`  
a reference to the actual DOM element that can be used to add event listeners, find other elements inside or modify the element itself.

### Use mixins to share behavior between components

Gremlin.js does not offer too much beside the very basics. That’s intentional, as it is __small and lightweigt__ this way.

To extend and to share code across your components you can use mixins. Gremlin.js supports inheritance as well, but for me, mixins are the preferred way to go.

A (currently small) __list of mixins__ available can be found here: [http://grml.in/modules/](http://grml.in/modules/). I do use them all the time, as they take care of those most important always repeating tasks you have to deal with when developing fancy JavaScript elements for a website.

The hello world example from a above gets even easier with the [jQuery mixin](https://github.com/grmlin/gremlins-jquery):

```javascript
const gremlins = require('gremlins');
const gremlinsJquery = require('gremlins-jquery');

gremlins.create('hello-world', {
  mixins: [gremlinsJquery],
  events: {
      'click button': 'onClick'
  },
  onClick(){
    alert('hello world!');
  }
});
```

There is also [gremlins-data](https://github.com/grmlin/gremlins-data) to read and parse (data) attributes, and [gremlins-dispatcher](https://github.com/grmlin/gremlins-dispatcher) for communication between components.

<blockquote class="twitter-tweet" lang="de"><p lang="en" dir="ltr">Seems they can talk to each other! <a href="https://twitter.com/hashtag/lt?src=hash">#lt</a></p>&mdash; DECAF (@_DECAF) <a href="https://twitter.com/_DECAF/status/672764772312588288">4. Dezember 2015</a></blockquote> <script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

----

## Remember: it’s not for web apps

__Gremlin.js is not a web app framework.__ It does not give you fancy data binding, history pushstate routing, models and all the other shiny things you need for an app. There are _a lot_ of options out there that do an awesome job at building apps (I prefer React).   

__Gremlin.js is build to help developers organize their ~~jQuery~~ JavaScript code on server-side driven websites.__ And it works. Write custom elements, add the corresponding CSS in BEM-style modules and you can reuse all your components with ease in other projects.

![Dancing](https://i.giphy.com/T7qkJ23gHGACs.gif)

<small>Source: [giphy](https://gph.is/1QtAHyR)</small>
