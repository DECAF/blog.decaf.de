---
layout: post
title: Grunt-Workflow für REDAXO CMS
featured: true
description: Beispiel einer REDAXO-Installation innerhalb eines Grunt-Workflows.
image: /content/images/2015/02/grunt-redaxo.png
author: ds
---

![grunt-redaxo](/content/images/2015/02/grunt-redaxo.png)

Wir haben unseren [Grunt](http://gruntjs.com/)-Workflow darauf ausgerichtet, gut mit [REDAXO CMS](http://www.redaxo.org/) zu können. Gleichzeitig sollte er möglichst generisch sein, um auch in anderen Umgebungen zu funktionieren — etwa WordPress, Magento/OXID, Applikationen auf Basis von [Laravel](http://laravel.com/), kleine Websites ohne Backend — oder ganz wichtig, weil wir das häufig für extern machen: um auch mal nur Frontend zu liefern.

Der Workflow ist nun seit vielen Monaten im Einsatz und schlägt sich wacker, deshalb haben wir ihn neulich in einer kleinen REDAXO-Demo auf Github veröffentlicht:

→ [github.com/DECAF/REDAXO-Grunt-Demo](https://github.com/DECAF/REDAXO-Grunt-Demo)

Nun sind solche Grunt-Setups durchaus komplex, und es hängen diverse Komponenten dran, die erstmalig installiert und eingerichtet werden müssen (siehe [README](https://github.com/DECAF/REDAXO-Grunt-Demo/blob/master/README%20setup.md)). Es handelt sich also nicht um ein Paket, das im Vorbeigehen lauffähig ist, sondern es benötigt einigen Aufwand, um es zum Laufen zu bekommen, es zu verstehen, es nützlich zu finden und — hier kommt der eigentliche Sinn der Sache: — damit effizient arbeiten zu können.

> This is an obsession, Dad. I’ve never understood it. Never. Neither did Mom.  
> <small>Indiana Jones in Indiana Jones 3</small>

Will sagen: Eigentlich müsste man einiges dazu besprechen, Hintergründe erklären und manche Themen herausstellen, die einem schnellen Wandel unterliegen oder von Entwicklern sehr unterschiedlich gehandhabt werden, etwa: [Compass](http://compass-style.org/) ja-nein-warum, Icons als SVG oder Fonts, [Autoprefixer](https://github.com/nDmitry/grunt-autoprefixer) und Browserkompatibilität, wieviel [Coffee](http://coffeescript.org/) ist gesund, warum überhaupt REDAXO. Sowas halt, ihr wisst schon.

**Es wäre also eine Diskussion nötig, und kein schlichtes Veröffentlichen von Code und langer [README](https://github.com/DECAF/REDAXO-Grunt-Demo/blob/master/README%20workflow.md).**

> Our situation has not improved.  
> <small>Professor Henry Jones in Indiana Jones 3</small>

---

## Ping!

Wer nun also Interesse an dem Thema hat, weil er/sie etwa REDAXO verwendet und die Entwicklung etwas automatisieren möchte oder ein kleines Entwicklungsteam aufbaut, gemeinsam an einem REDAXO-Projekt arbeitet oder irgendwas der gleichen plant, mag uns gerne anpingen. Stellt ruhig Fragen, macht Verbesserungsvorschläge, diskutiert Sinn und Unsinn solcher Workflows. Bei Interesse stelle ich den Workflow auch gerne mal live vor, etwa beim nächsten REDAXO-Treffen.

Kontaktmöglichkeiten:

- Twitter: [@_DECAF](https://twitter.com/_DECAF)
- Github: [Issues](https://github.com/DECAF/REDAXO-Grunt-Demo/issues)
- REDAXO-Forum: [Diskussion](http://www.redaxo.org/de/forum/php-html-css-mysql-f9/grunt-redaxo-t19988.html)  *(Zum Schreiben ist eine Registrierung erforderlich)*
- E-Mail an mich: [ds@decaf.de](mailto:ds@decaf.de)
- ~~Kommentare zu diesem Blogartikel~~
