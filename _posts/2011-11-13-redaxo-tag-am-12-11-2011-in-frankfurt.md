---
layout: post
title: REDAXO-Tag am 12.11.2011 in Frankfurt
description: "Bericht vom REDAXO-Tag in Frankfurt: Über TOXID, XForms Manager + Community und dem anstehenden REDAXO 5."
image: /content/images/2015/02/redaxotag.jpg
author: ds
more: true
---

Um [REDAXO](http://redaxo.org) ist es in den letzten Monaten etwas stiller geworden als üblich, was daran liegen kann, dass das Team in der Entwicklung der neuen **Version 5** steckt. Es gab Pläne, die 5er schon zu Beginn dieses Jahres zu veröffentlichen, als es dann aber zu Verzögerungen kam, hat man beschlossen, den gewohnten Weg zu gehen: *Es kommt dann, wenn es fertig ist*. Inzwischen wird es immer fertiger, so dass angekündigt wurden, den aktuellen Stand auf dem REDAXO-Tag in Frankfurt vorzustellen.

---

### TOXID

Vorher gab es noch Vorträge aus dem 4er-Umfeld. [GN2](http://www.gn2-netwerk.de) zeigte mit Joscha Krugs **[TOXID](http://www.toxid.org/)** einen Weg, den OXID-Webshop mit REDAXO zu paaren, um die beschränkten CMS-Fähigkeiten des Shopsystems aufzubohren. TOXID unterstützt übrigens auch TYPO3, WordPress und andere Systeme. Die Inhalte wandern dabei als XML in OXID.

---

### XForms Manager + Community Addon

![Foto](/content/images/2015/02/redaxotag.jpg)

[Yakamara](http://www.yakamara.de) demonstrierte den **XForms Manager**, das neue Allzweckmittel für jegliche Form von tabellarischen Daten, die von Redakteuren gepflegt werden können. Das Addon erinnert an Drupals [CCK](http://drupal.org/project/cck) und ermöglicht ein Zusammenklicken von Datenfeldern samt Relationen. Beispiel aus der Praxis: Um ein Nutzerverzeichnis zu erstellen, werden Gruppen angelegt, danach eine Eingabemaske mit typischen Feldern wie Name, E-Mail-Adresse und Standort generiert und sinnvoll verknüpft. Der XForm Manager stellt dafür alle Werkzeuge bereit und erweitert die Datenbank.  
 Diese Möglichkeiten sind schon überaus praktisch, aber es sollte noch besser kommen. Denn auch das neue **Community-Addon** wurde vorgestellt, das in Verbindung mit den XForms dafür sorgt, dass Prozesse um den neu geschaffenen Datenbestand entwickelt werden können wie z.B. Registrierung, Login und gängige Features zur Nutzerverwaltung.  
 Das alles gab es auch vorher schon, nur war es längst nicht so einfach zu handhaben und erforderte viel eigene Entwicklungsarbeit, so dass REDAXO mit den nativen Möglichkeiten, die z.B. Drupal bietet, kaum mithalten konnte. Die beiden Addons rund um XForms und Community sind jedoch ein wichtiger Schritt in diese Richtung, und die anwesende Community war entsprechend begeistert von der Demonstration.

Kleines Zwischenfazit an dieser Stelle: REDAXO wird immer erwachsener und geschickter darin, mit Datenbeständen zu hantieren. Für den Redakteur jedoch bleibt es einfach und sinnvoll, und das war schon immer der entscheidende Grund, warum das System so gerne eingesetzt wird. *Content is king*, und man sollte Redakteure nicht zu Hofnarren machen.

---

### Inhalte als JSON, Tagging, Facebook Connect

Weitere Vorträge. [Pascal Szewczyk](http://www.peppmedien.de) zeigte, wie REDAXO auf einer [Microsite von DerWesten](http://envio.derwesten.de) zum Einsatz kommt. Sie benötigt alle **Inhalte als JSON**, und natürlich kann REDAXO die liefern.

[Joachim Dörr](http://www.doerr-softwaredevelopment.com) demonstrierte eine **Portfolio-Website**, deren Inhaltsstrukturen primär über Verschlagwortung abgebildet werden. Kampagnen gehören zu Projekten, Projekte gehören zu Kunden, Kunden stecken in Gruppen. Und das alles wird wild getaggt. Sehr schön umgesetzt!

[Christophe Vouillamoz](http://www.profil1.ch/profil1.html?member=41) zeigt danach, wie **Facebook Connect** in eine REDAXO-Umgebung integriert werden kann, um all die Social-Dingse an eine Website kleben zu können, die Facebook anbietet. Christophe hat dafür ein Addon entwickelt, das feiner nicht sein könnte. Respekt und großes Interesse seitens der Community.

[Oliver Kreischer](http://kreischer.de) demonstrierte sein **Basismodul zum Umgang mit Bildern**, GN2 erklärte ihr Vorgehen auf einer Website mit **Buchrezensionen**. Und überhaupt wurde auch in den Gesprächen untereinander viel über **Best Practices** im Umgang mit dem CMS gesprochen.

---

### REDAXO 5

Jetzt endlich REDAXO 5. Jan demonstriert den aktuellen Stand und erklärt, was gemacht wurde und welche Ziele verfolgt werden:

- Der **Core** soll so schlank wie möglich gehalten werden.
- Nahezu sämtliche Funktionalität dockt zukünftig als **Addon** an. Auch vieles von dem, was vorher Kernfunktionalität war.
- Zukünftiges **Releases** sollen damit schnell möglich sein und klein gehalten werden.
- Es gab ein umfangreiches **Refactoring**, viele Altlasten wurden entfernt. Basis ist PHP 5.3.
- **Neue GUI**: Aufklappbarer Seitenbaum, Drag & Drop, Themes. Sehr schick und fokussiert!
- Aus dem Image Manager wird der **Media Manager**: Neue Möglichkeiten für Dateihandling, Rechtemanagement, Caching.
- **Software-Updates** direkt im Backend: Vom Server erhalten (Core, Packages) und — oho! — zum Server pushen. Konkret: Plugin-Releases werden per Klick erstellt und veröffentlicht.
- Ein **Compat-Modus** für REX 4-Websites
- Wechsel von SVN zu **GitHub**: Transparenz und Möglichkeiten der Community zur Mitarbeit

Die brennende Frage an dieser Stelle: Wann wird REX 5 veröffentlich? Jan hat sich zu einer recht konkreten Antwort verleiten lassen (*Hint: Kleine Zahl, Einheit Monate*), aber vielleicht ist es besser zu sagen: Wenn es fertig ist.

Wir haben das Gefühl, es wird richtig gut.

[![Tweet](/content/images/2015/02/redaxotag.png)](http://twitter.com/#!/jackomono/status/135370781608775680)

---

Danke an Yakamara und alle Helfer für die Organisation und an alle Beteiligten für die guten Vorträge und netten Gespräche. Es war eine großartig entspannte Stimmung!

---

### Ergänzende Links:

- [GitHub: REDAXO 5 Repo](https://github.com/redaxo/redaxo)
- [GitHub: Änderungen in REDAXO 5](https://github.com/redaxo/redaxo/wiki/Änderungen-in-REDAXO-5)


