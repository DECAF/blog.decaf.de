---
layout: post
title: Ghost 0.6, Einsnull und WordPress
image: "/content/images/2015/04/ghost-0-6.png"
date: '2015-04-14 13:37:40'
tags:
- wordpress
- tryghost
---

Gestern wurde [Ghost 0.6.0 veröffentlicht](http://dev.ghost.org/ghost-0-6-0/). Ein Minor-Update (von 0.5.10) mit nur wenigen neuen Features:

![Ghost 0.6.0](/content/images/2015/04/ghost-0-6.png)

* __Autokorrektur im Editor__ (»Spellcheck«)
* __Uploads in Mobilgeräten__ (»Mobile uploads«)
* __Links zum Blättern: Vorheriger Beitrag, nächster Beitrag__ (»Next & previous post helpers«)
* __Einfügen von Code in Header und Footer aus dem Adminbereich heraus__ (»Code injection«)
* __Speicherort für Bilder konfigurierbar__ (»Customisable image storage«)

Auch das hauseigene [Casper-Theme](https://demo.ghost.io) entwickelt sich weiter und nimmt die neuen Links zum Blättern als neues Feature mit auf.

Unser Blog basiert übrigens auf Casper. Wir haben es modifiziert, um weniger magazinartig zu sein. Casper arbeitet mit großflächigen Artikelbildern — kennt man von [Medium](https://medium.com) —, und das passt leider so gar nicht in unseren Workflow; wir sind eher kurz und textlastig. Außerdem wollten wir Inhalte mit drin haben, die wir parallel z.B. bei [Twitter](https://twitter.com/_DECAF) posten.

Wir müssen das Theme bei Updates von Casper also manuell nachziehen, falls gewollt. Denn Ghost kann keine Child-Themes, so wie WordPress, die das Eltern-Theme updatefähig belassen.
<br>

## Ghost als Ersatz für WordPress?

Wie schlägt sich Ghost in der aktuellen Version eigentlich im Vergleich zu WordPress?  
Aus meiner Sicht: Ghost fehlt noch ganz viel Funktionalität, die WordPress schon seit langer Zeit mitbringt, und Ghost wird manches davon vermutlich gar nicht integrieren wollen. Während sich WordPress im Laufe der Jahre zu einem umfangreichen CMS entwickelt hat, mit dem man bei Bedarf große Newsportale oder Websites von Universitäten (In Deutschland etwa https://www.fau.de) realisieren kann, fokussiert sich Ghost aktuell noch aufs reine Bloggen.

__Nochmal konkret: Was kann WordPress, was Ghost aktuell nicht kann?__

* __Medienpool__  
Ghost hat keinen. Und auch keinen Bildgenerator für Thumbnails. Und auch keine Funktionalität, um aus ausgewählten Bildern Galerien zu erstellen.  
In Ghost könnt ihr Bilder einzelnd hochladen und direkt verwenden. Ganz raw mittels Folder und Dateinamen, nicht etwa dynamisch per ID verknüpft oder sowas. Ghost hat quasi nur einen Upload-Helper, der am Ende Markdown rauswirft. Das Bild ist nach Upload keine bekannte Ressource des Systems mehr.
* __Kommentare__  
Müssen bei Bedarf extern abgehandelt werden, etwa über [Disqus](https://disqus.com).
* __Plugins__  
Heißen bei Ghost _Apps_. Most wanted feature. Wird vermutlich noch ein ganzes Weilchen benötigen.
* __API__  
In Arbeit, hell yeah!
* __Kategorien__  
In Ghost gibt es nur Tags, keine Kategorien.
* __Themeoptionen, Child Themes, Widgets__  
Kernfeatures von WordPress, die Ghost leider nicht mitbringt. Themeoptionen und Widgets fände ich hier auch unpassend, weil sie die Kontrolle von Funktionalität auf die Anwender\_innen übertragen, die vielleicht besser bei den Entwickler\_innen aufgehoben ist.  
Child Themes allerdings sind sehr praktisch und irgendwie auch notwendig für den Fall, dass sich um Ghost auch mal ein so großer Theme-Wald entwickeln soll wie bei WordPress.
* __Formatvorlagen, Sichtbarkeit, zeitgesteuertes Publizieren, Revisionen…__  
Diverse Funktionalität innerhalb der Beiträge von WordPress gibt es in Ghost nicht. Manches wird vielleicht noch kommen, aber grundsätzlich bleibt es wohl eher reduziert _(fokussiert!)_.
* __Multisite__  
Ein Ghost, ein Blog.

Mehr fällt mir gerade nicht ein. Falls ihr ergänzen möchtet, gerne! [@_DECAF](https://twitter.com/_DECAF)
<br>

#### By the way…

Interessant übrigens: Die Firma hinter Ghost macht aktuell einen Umsatz von __411.000 Dollar__ pro Jahr. Denn es gibt bereits 3764 Nutzer\_innen, die Ghost als kostenpflichtigen Service hosten lassen, ähnlich wie wordpress.com. Diese Kennzahlen wurden neulich [veröffentlicht](http://blog.ghost.org/april-2015-update/) und sind zukünftig über das _Public Revenue Dashboard_ einsehbar. Neben der Entwicklung von Ghost lässt sich nun also auch die Entwicklung des Unternehmens hinter Ghost verfolgen — sehr spannend!

Automattic, die Firma hinter WordPress, veröffentlicht keine Kennzahlen in der Form, jedoch lässt sich die Dimension erahnen, wenn man sich mit dem Funding beschäftigt: Im letzten Jahr hat Automattic eine Finanzspritze von 160 Millionen Dollar erhalten und ist damit (auf dem Papier) mehr als eine Milliarde Dollar wert. (Quelle: [Matt](http://ma.tt/2014/05/new-funding-for-automattic/))
Für 2012 — bereits ein Weilchen her — wurde ein Umsatz von 45 Millionen Dollar erwartet. (Quelle: [allthingsd.com](http://allthingsd.com/20120425/automattic-grows-up-the-company-behind-wordpress-com-shares-revenue-numbers-and-hires-execs/))

Aber zurück zu Ghost:
<br>

## Ghost: Nächste Features?

Was bei Ghost passiert, lässt sich sehr gut verfolgen:

1. Git commits: [Ghost](https://github.com/TryGhost/Ghost/commits/master), [Casper-Theme](https://github.com/TryGhost/Casper/commits/master).
2. [Roadmap auf Trello](https://trello.com/b/EceUgtCL/ghost-roadmap)
3. [Git issues und deren Diskussionen](https://github.com/TryGhost/Casper/issues)
3. [Dev Blog](http://dev.ghost.org)
4. [Allgemeines Blog](http://blog.ghost.org)

Die nächsten Features werden laut Trello (in dieser Reihenfolge) sein:

* __Query helper in den Themes__ [#4439](https://github.com/TryGhost/Ghost/issues/4439)  
Klasse, damit wird die JSON API angezapft und ermöglicht in den Themes ganz viele Dinge, die bisher nicht oder nur schwerlich sinnvoll gingen, wie z.B. Tags auflisten, andere Artikel abfragen, einen Index erstellen, o.ä.
* __Passwortschutz für Blogs__ [#4993](https://github.com/TryGhost/Ghost/issues/4993)  
Beachten: Fürs ganze Blog, nicht für einzelne Artikel des Blogs.  
Ein Passwortschutz für Artikel ist aktuell nicht vorgesehen, sowas wird man später mittels App (Plugin) bauen müssen.
* __Artikelvorschau (Preview)__ [#4595](https://github.com/TryGhost/Ghost/issues/4595)    
Sehr schön, die fehlte wirklich. Zwar zeigt der Markdown-Editor bereits eine HTML-Vorschau im Adminbereich, aber es gab bisher keine Möglichkeit für die Voransicht eines Artikels innerhalb der späteren Blogumgebung.
* __Lokalisierung und Internationalisierung (l10n/i18n)__ [#3801](https://github.com/TryGhost/Ghost/issues/3801)  
Ghost soll mehrsprachig werden. Das betrifft zwei Bereiche: Zum einen können Nutzer\_innen auswählen, in welcher Sprache sie Ghost im Adminbereich bedienen möchten. Zum anderen aber kann auch die Sprache des Blogs selbst konfiguriert werden, was Einfluss darauf hat, wie ein Datum ausgegeben wird, wie Pluralformen gebildet werden (falls Helper benutzt werden) oder wie Slugs aussehen (etwa für Tags, Authors oder Pages).  
Nicht vorgesehen ist aktuell die Möglichkeit, ein Blog in mehreren Sprachen zu betreiben. Dies wird man später mittels App (Plugin) lösen müssen, so wie es auch bei WordPress der Fall ist.
* __API__ [#4004](https://github.com/TryGhost/Ghost/issues/4004)  
Oh ja, bitte. Die API wird Ghost für ganz viel Custom-Funktionalität öffnen — vorerst innerhalb der Themes — und ist notwendig für die späteren Apps (Plugins).

Sehr schön. Tolle neue Features, my dear!

---

### Fazit?

Ghost ist technisch längst noch kein vollwertiger Ersatz für WordPress und wird es vorerst auch nicht werden. Ghost fehlt ein ganzer Haufen von Funktionalität, die WordPress zu einem Allround-CMS macht, während Ghost ein schlichtes Blogsystem ist.

Der nächste große Schritt für Ghost wird sein, die API und die Apps (Plugins) an den Start zu bringen. Damit kann sich das System öffnen und schlagartig für viele Anforderungen geeignet sein.
— Das Feature _Apps_ jedoch liegt noch im Backlog, wird also nicht so bald umgesetzt werden.

Du kannst dein Blog von WordPress auf Ghost umstellen, wenn du nur wenig Funktionalität benötigst. Das haben wir auch gemacht, der Aufwand dafür war überschaubar.  
Beachte aber: Du benötigst ein Node-Hosting. Das ist aktuell längst nicht so einfach zu kriegen wie ein typischer PHP/MySQL-Stack für WordPress. Wir lassen bei Uberspace hosten. Funktioniert prima, und die Einrichtung ist gut [dokumentiert](https://wiki.uberspace.de/cool:ghost).

Subjektiv zum Abschluss: Ghost. rockt. sehr.