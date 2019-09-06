---
layout: post
title: 'Windows 8 App-Entwicklung: All mite long.'
featured: true
description: Wie wir 2013 versucht haben, Windows-8-Apps auf Basis von JavaScript zu entwickeln. Und am Ende stand ein lahmes Pferd.
image: /content/images/2015/02/allmite_01.png
author: ds
more: true
---

Ein Rückblick. __2013__ haben wir einige Zeit mit App-Entwicklung für Windows 8 verbracht. Denn wir waren recht überzeugt davon, dass Microsoft ein ganz nettes System erschaffen hatte. Zumindest das Konzept und die Basis eines netten Systems, denn was die Ausführung angeht, gilt immer die alte Regel: Finger weg vom ersten Release eines Produkts!

Die Voraussetzungen waren einfach zu perfekt: Mit Windows 8 wurde möglich, __native Apps auf Basis von JavaScript__ zu entwickeln; für das verbreitetste Betriebssystem von allen! Zudem hat Microsoft viel dafür getan, Entwickler\_innen von Anfang an zu unterstützen: Es gab Mengen von guten Inhalten, Sourcecodes, Demos, Tutorials, sogar kostenlose Fachbücher, geschrieben von Core-Entwicklern\_innen. Es wurden Veranstaltungen organisiert und Coworking-Spaces eingerichtet, in denen man in einer Umgebung von Microsoft-Techies an Apps arbeiten konnte. Das und ganz viel mehr.
Runtergebrochen: Wer sich für App-Entwicklung für Windows 8 interessierte, musste vor allem JavaScript können — _und hell yeah, das konnten wir_ —, brauchte aber keine Angst haben, sich in der Entwicklungsumgebung zu verlieren. Hilfe war jederzeit greifbar.

<blockquote class="twitter-tweet" lang="de"><p>Any Javascript people want to make a Windows 8 app with me?</p>&mdash; Peter Coffin (@petercoffin) <a href="https://twitter.com/petercoffin/status/300442116977467392">10. Februar 2013</a></blockquote>
<script async src="//platform.twitter.com/widgets.js" charset="utf-8"></script>

Die Chancen standen gut, dass die Sache mit den Apps und Windows 8 klappen würde. Wir haben uns für den Einstieg eine kleine App für den Arbeitsalltag ausgedacht, mit der wir starten wollten: Die [mite](http://mite.yo.lk)-API anfragen und Arbeitszeiten nach Soll und Ist auswerten. Aufzeigen also, wie viele Überstunden jemand hat.

Die App bekamen den Namen __Allmite__, der sich später als schon belegt rausstellen sollte, aber erstmal gut klang. Allmite als Variante von Almitey (Almighty), der oder die Allmächtige mit dem Blick von oben auf alle Zahlen.

__Ich zeige euch ein paar Screens, bevor wir dazu kommen, warum das Ding am Ende in die Tonne getreten und die Nummer mit der App-Entwicklung für Windows 8 gecancelt wurde:__

---

## Allmite

![Screenshot 1](/content/images/2015/02/allmite_01.png)

Die Hookline:

> Mit allmite überblickst du dein mite-Stundenkonto: Es zeigt deine Zeiteinträge in übersichtlicher Monatsdarstellung und berechnet, ob du im Soll bist.  
> Das ist nützlich für Festangestellte. Und für Freelancer, die ~~zuwenig~~ zuviel arbeiten.

So sah es auf einem Notebook aus:

![Screenshot 2](/content/images/2015/02/allmite_02.png)

Noch ein Screen des Benutzerkontos auf einem Surface:

![Screenshot 3](/content/images/2015/02/allmite_03.png)

Und falls ihr den letzten Stand der Website sehen möchtet, von der die Screenshots stammen:
**http://allmite.decaf.de/**  _(User: `test`, Pass: `mighty`)_

---

### Ende

Wie man sehen kann, waren wir recht nah dran, die App fertigstellen zu können. Und dann wurde es Schritt für Schritt komplizierter:

* Der Name war belegt.  
_(Kein Problem, wir hätten einen anderen gefunden.)_  

* Es hätten mindestens noch Feiertage für Österreich und die Schweiz eingepflegt werden müssen.  
_(Fleißarbeit, hätten wir hinbekommen.)_  

* Schweizerische Feiertage sind nicht ganz trivial. Das dahintersteckende System erstreckt sich über [einen langen Wikipedia-Artikel](http://de.wikipedia.org/wiki/Feiertage_in_der_Schweiz), und am Ende ist nichts, wie es scheint.  
_(Okay, nicht nur für die Schweiz: Wir hätten Feiertage vom Benutzer editierbar machen müssen. Zusatzaufwand, aber das hätten wir schon hingekriegt.)_  

* Nach Veröffentlichung dieser kostenlosen App hätten wir Support leisten und mindestens die nächsten zwei Releases mit noch fehlenden Features und möglichen Bugfixes rausbringen müssen.  
_(Verdammt, die Sache fing an, arg aufwendig zu werden.)_

__Bis hierher hätten wir es noch durchgezogen, dann aber kamen die echten Showstopper:__

* Windows 8 überzeugte uns nicht. Im Laufe der App-Entwicklung wurde uns das immer klarer.
* Windows 8 überzeugte die Nutzer\_innen da draußen offenbar nicht.
* Windows 8 überzeugte offenbar auch unsere potentiellen Kunden nicht. Wir wussten etwa von Verlagen, die Budgets ausgeschlagen haben, und keine App entwickeln wollten.
* Mit Windows 8.1 schien das irgendwie nicht besser zu werden.

<iframe src="//giphy.com/embed/DO9WQFLaAEnM4?html5=true" width="480" height="356" frameBorder="0" webkitAllowFullScreen mozallowfullscreen allowFullScreen></iframe>
<cite><small>– [giphy.com](http://giphy.com/gifs/reaction-reactiongifs-steve-DO9WQFLaAEnM4)</small></cite>

Am Ende stand die Vermutung, auf ein ~~zahmes~~ lahmes Pferd gesetzt zu haben, und wir haben die App nicht weiter verfolgt. Als einzelnes Projekt war es sehr spannend, wir haben viel gelernt und waren zwischenzeitlich beinahe euphorisch darüber, welche gute Arbeit Microsoft aus Entwicklersicht geleistet hatte. Aber für langfristig sollte das besser nicht unser Ding werden.

— [Lesson learned](https://www.youtube.com/watch?&v=RkTkZQvZxos#t=63). ¯\\_(ツ)_/¯
