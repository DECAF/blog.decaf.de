---
layout: post
title: Look ma, new blog!
description: "Wir haben ein neues Blog, in dem man schnell schreiben kann. Mit Markdown. Es basiert auf Ghost, und das ist ziemlich schlank und toll."
image: /content/images/2015/02/ghost-org.jpg
author: ds
more: true
---

__Das wurde jetzt wirklich Zeit.__ Wir haben den kühnen Plan, unsere Website neu zu machen. Sie ist von 2008; und das ist nicht mal mehr alt, sondern — für eine Website – eigentlich schon verwest.

Dann fiel mir ein, dass da auch noch ein Blog dranhängt, in dem niemand mehr schreibt. Warum eigentlich nicht?

![DECAF-Blog bis gestern](/content/images/2015/02/decaf-blog-2008.jpg)

__Ausrede 1:__ Weil die technische Umgebung keinen Spaß macht. Nichts gegen WordPress _— na gut, das ein oder andere gäbe es da schon —_, wir nutzen es gerne für Kundenprojekte. Für unser eigenes Blog jedoch ist es viel zu aufgeblasen. Zudem muss es so regelmäßig gepflegt werden wie unser Bonsai im Büro. _(Er wird durch den Winter kommen.)_

__Ausrede 2:__ Weil es schlecht mit kurzen Inhalten klarkommt. Und kurze Inhalte sind unser Ding; wir können schlecht lang.

Um nicht weiter in Ausreden zu flüchten, gibt es nun einfach ein neues Blog. Eins, in dem man schnell und kurz schreiben kann, weil es Markdown akzeptiert und fürchterlich schlank ist: [Ghost](https://ghost.org).

---

### Ghost?

[![Ghost.org](/content/images/2015/02/ghost-org.jpg)](http://ghost.org)

Ghost ist zum aktuellen Zeitpunkt (0.5.8) noch sehr rudimentär. Es fehlt fast alles, was man erwarten möchte, wenn man von einem WordPress rüberwechselt.

Es gibt bisher weder __Apps__ (Plugins) noch eine __API__. Dementsprechend wandert sämliche Funktionalität noch in die __Themes__; und auch hier kann man gerade nicht allzu viel tun, weil nur beschränkte Daten zur Verfügung stehen. Die Pages (die Einzelseiten) z.B. haben keinen Zugriff auf die Posts-Daten, so dass es aktuell kaum sinnvoll möglich ist, durch alle Posts zu loopen, um etwa ein Inhaltsverzeichnis aufzulisten.  
— Ghost ist fürchterlich beschränkt.

Gleichzeitig macht es Spaß zu beobachten, wie wenig Ghost aktuell kann. Denn wenn man durch die [Github-Issues](https://github.com/TryGhost/Ghost/issues) und die kargen [Docs](http://docs.ghost.org) liest, erfährt man bald, woran es liegt: Sie wollen alles richtig machen. Sie wollen neue Features nicht einfach raushauen, nur weil sie schnell umgesetzt werden könnten.  
Am Beispiel der Posts-Daten oben: Natürlich _könnte_ man die Daten ohne viel Aufwand auch den Pages zur Verfügung stellen — es wäre nur ein kleines Schnipselchen Code dafür nötig (siehe auch [#1158](https://github.com/TryGhost/Ghost/issues/1158)). Allerdings hätte das großen Einfluss auf die Performance, und man mag ahnen, was daraus entwächst, wenn Nutzer kreativ mit ihren Möglichkeiten umgehen: Ich hätte jenes Inhaltsverzeichnis direkt im Theme erstellt. Stattdessen bin ich nun gezwungen, den ordentlichen Weg zu gehen, sobald er zur Verfügung steht: eine App bauen, die die API anzapft.

---

### Fazit

Wir haben ein neues Blog, in dem man schnell schreiben kann.  
Und:

Ghost ist aktuell (0.5.8) noch nicht weit genug, um es auf typische Blogprojekte loszulassen. Es fehlen mindestens die Apps und die API. Und im Detail stößt man regelmäßig auf Features, die einem fehlen, wenn man WordPress gewohnt ist.

Aber auch, wenn Ghost sich demnächst ein paar Schritte weiter entwickelt hat, wird es damit für die Masse der Entwickler_innen und Dienstleister vermutlich nicht schlagartig interessant sein. Denn ein Node-Ding hostet sich längst nicht so einfach wie ein typisches PHP-Etwas. Auch wenn manche Hoster bereits damit klarkommen, ist es nicht damit getan, Sourcen irgendwo abzulegen, um Dinge zum Laufen zu bekommen.

Abgesehen davon: Ghost ist fürchterlich schick und reduziert. Das ganze Gebimmel rund um ein typisches WordPress-Blog entfällt, und wer möchte, kann gleich viel freier atmen.
