---
layout: post
title: 'Blog-Navigation: Paging'
description:
author: ds
---


*Dies ist Teil 1 des Artikels über Blog-Navigation. Siehe auch Teil 2: [Paging (2)](http://blog.decaf.de/2008/01/31/blog-navigation-paging-2).*

Das typische Paging in Weblogs beschränkt sich meist auf die beiden Links »weiter« und »zurück« bzw. »ältere Artikel« und »neuere Artikel«. Aufwendigere Varianten – für WordPress einfach mittels Plugin erweiterbar – enthalten Seitenlinks samt der Information darüber, wie viele Seiten das Blog enthält. Häufig sieht das etwa so aus:

![Navigation 1](/content/images/2015/02/navigation_01.png)

Lässt sich damit nun komfortabler blättern? Grundsätzlich schon, denn der Nutzer kann bei Bedarf größere Sprünge machen – etwa dann, wenn er als regelmäßiger Leser des Blogs weiß, dass ein Artikel, den er sucht, nicht mehr auf den ersten drei Seiten steht – oder gleich zur letzten Seite des Blogs springen, um z.B. die gesamte Entstehungsgeschichte nachzuholen *(Hum?)*.  
 Jedoch ist das oben gezeigte Navigationsbeispiel nicht optimal. Mal sehen, ob es sich verbessern lässt..

### Das Paging verbessern

**Schritt 1: Links entfernen, die keine sind**  
 Alle Elemente sehen klickbar aus, obwohl es zwei nicht sind: »Seite 2 von 287« ist eine reine Information, kein Link, und auch die teilenden Pünktchen »…« sind nicht klickbar. Weg mit den Rahmen:

![Navigation 2](/content/images/2015/02/navigation_02.png)

**Schritt 2: Wichtige Aktionselemente verstärken**  
 Die beiden wichtigsten Elemente im täglichen Gebrauch sind vermutlich die Links zum seitenweise Vor- und Zurückblättern. Auch wenn ein hoher Anteil von Nutzern den direkten Klick auf die Seitenzahl bevorzugen wird, haben die Blättern-Links den entscheidenen Vorteil, dass man bei der Benutzung nicht nachdenken muss. Das klingt etwas abwegig, weil es sich doch allein um simple Zahlen handelt, die zu treffen sind, jedoch zeigen die Uhrzeit dieses Postings und der erste Screen der Navigation oben recht gut, welche Faktoren den Prozess beeinflussen können: die Aufmerksamkeit des Benutzers – um diese Zeit durchaus gering – und die schlechte Kennzeichnung der aktuellen Seite 2. Um also die 3 als nächste Seite zu treffen, muss ich hier merkliche Energie aufwenden, während sich die Blättern-Links in der Regel recht »blind« und intuitiv bedienen lassen. Mit »Blind« meine ich, dass man seitenweise blättern kann, wenn der Mauszeiger auf dem Knopf gehalten und ohne zu Gucken geklickt werden kann – das ist in Blogs aufgrund der langen Seiten allerdings kaum möglich, wenn vorher gescrollt werden muss.  
 Mehr Fokus auf wichtige Elemente also. Zuerst durch ihre Größe:

![Navigation 3](/content/images/2015/02/navigation_03.png)

Danach durch ihre Farbe:

![Navigation 4](/content/images/2015/02/navigation_04.png)

**Schritt 3: Unwichtige Aktionselemente zurücknehmen**  
 Als Konsequenz aus dem letzten Schritt empfinde ich einen Link als den unwichtigsten von allen, weil er zwar *nice to have* ist, jedoch im täglichen Gebrauch eher selten verwendet wird: den Link auf die letzte Seite des Blogs. Im aktuellen Screen hat er recht viel Relevanz, weil er aufgrund seiner Größe und seiner Position ganz außen besser wahrgenommen wird als die inneren Elemente. Etwas weniger Aufmerksamkeit könnte nicht schaden. Zuerst nur durch Anpassung der Größe; die Position wird dann im übernächsten Schritt nochmal aufgegriffen:

![Navigation 5](/content/images/2015/02/navigation_05.png)

**Schritt 4: Kennzeichnung des Status Quo**  
 Eben schonmal angesprochen und nun auf dem Weg zur Ausbesserung: die aktuelle Seite ist meiner Meinung nach längst nicht offensichtlich genug gekennzeichnet. Das erschwert die Navigation, deshalb sollten wir etwas Farbe nachlegen:

![Navigation 6](/content/images/2015/02/navigation_06.png)

**Schritt 5: Die Konsistenz verbessern**  
 Spricht man von einer *konsistenten* Navigation, will man darauf hinaus, dass sie *beständig* und *in sich geschlossen* ist. Will sagen: sie ist einheitlich, funktioniert auf jeder Seite nach dem gleichen Schema und steht immer an der gleichen Stelle.  
 Das Punkt des in sich Geschlossenen ist in unserer aktuellen Navigation noch nicht ganz ausgeprägt, denn während der Link zum Zurückblättern das erste Aktionselement bildet, steht der Link zum Weiterblättern zwischen anderen Aktionselementen. Das ist nicht falsch, und die Abfolge lässt sich auch prima begründen, indem man den Link zur letzten Seite als logisch abschließendes Element betrachtet. Geschlossener und dabei gleichfalls logisch ist es jedoch, wenn der Link zur letzten Seite eingegliedert wird und damit der Blättern-Link den Abschluss bildet. Dadurch erhält er zudem mehr Aufmerksamkeit und der Link zur letzten Seite weniger, so dass Schritt 3 von eben nochmal sauber abschließen kann. Zudem unterstützt die Position der Blättern-Links nun ihre Funktion: ganz rechts führt es weiter, ganz links zurück:

![Navigation 7](/content/images/2015/02/navigation_07.png)

---

### Resultat

Die beiden primären Aktionselemente haben mehr Aufmerksam erhalten und befinden sich nun jeweils auf den äußeren Positionen, so dass sie annähernd gleichwertig sind und die Seitenlinks in der Mitte umschließen. Die aktuelle Seite wurde zudem deutlicher gekennzeichnet als zuvor und die gesamte Navigation ist hoffentlich intuitiver geworden.

---

### Weitere Artikel zum Thema

- [Blog-Navigation: Paging (2)](http://blog.decaf.de/2008/01/31/blog-navigation-paging-2)
- ~~[Blog-Navigation: Der »Artikel auf Seite x«-Link](http://blog.decaf.de/2007/04/blog-navigation-the-entries-on-page-x-link)~~

**Nachtrag:** Mathias Schäfer greift das Thema im SELFHTML-Blog auf: »[Usability von Seiten-Navigationen](http://aktuell.de.selfhtml.org/weblog/seitennavigation)«


