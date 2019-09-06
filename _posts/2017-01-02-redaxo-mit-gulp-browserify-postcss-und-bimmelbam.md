---
layout: post
title: REDAXO mit Gulp, Browserify, PostCSS und Bimmelbam
featured: true
description: Beispiel eines Frontend-Workflows zur Entwicklung einer REDAXO-Website.
image: /content/images/2017/01/redaxo-mit-bimmelbam.png
imageClass: seamless
author: ds
---

Bei den [Friends Of REDAXO](https://github.com/FriendsOfREDAXO/Info) haben wir gestern einen __Frontend-Workflow__ zur Entwicklung einer REDAXO-Website veröffentlicht. Die daraus generierte Website schaut dann so aus:

<a href="https://github.com/FriendsOfREDAXO/redaxo-mit-bimmelbam"><img class="seamless" src="/content/images/2017/01/redaxo-mit-bimmelbam.png" alt="Screenshot"></a>

## Komponenten und Funktionen

* [Yarn](https://yarnpkg.com) als __package manager__
* [Gulp](http://gulpjs.com) als __task runner__
* [Sass](http://sass-lang.com) und [PostCSS](http://postcss.org) für __CSS__ (mit [Autoprefixer](http://autoprefixer.github.io), [cssnano](http://cssnano.co) und Bimmelbam)
* ES2015 mit [Babel](http://babeljs.io) und [Browserify](http://browserify.org) für schönes __JavaScript__
* [Nunjucks](https://mozilla.github.io/nunjucks/) __Templates__ (für den Prototyp, könnten aber auch für JavaScript-Komponenten verwendet werden)
* ein konfigurierbarer [Modernizr](https://modernizr.com) (weil es geht)
* __Bilder__ werden minifiziert
* __SVGs__ werden kombiniert und ins HTML gebracht (für Icons)
* [Bootstrap](http://getbootstrap.com) und [Google Material Icons](https://material.io/icons/) werden als externe Komponenten (via npm) eingebunden
* [BrowserSync](https://www.browsersync.io) für __Live-Reload__ und zum Test auf verschiedenen Geräten

---

## Links zum Projekt

https://github.com/FriendsOfREDAXO/redaxo-mit-bimmelbam

__Anlaufstellen für Fragen, Anmerkungen oder bei Problemen:__

* Chat im [REDAXO-Slack](http://www.redaxo.org/slack/)
* Diskussion im [REDAXO-Forum](http://www.redaxo.org/de/forum/allgemeines-f39/frontend-workflow-fur-redaxo-mit-gulp-browserify-postcss-t21541.html)
* Twitter: [@_DECAF](https://twitter.com/_DECAF)
