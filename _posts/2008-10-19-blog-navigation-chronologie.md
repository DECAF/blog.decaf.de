---
layout: post
title: 'Blog-Navigation: Chronologie.'
description: "Du kannst in einem Blog nicht wie in einem Buch lesen, wenn der Weg zurück in die Chronologie fehlt. Unser WordPress-Plugin möchte das Problem beheben."
image: /content/images/2015/02/entries-on-page-x-link1-250x217.png
author: ds
more: true
---

Nochmal fünf Worte zum Thema **Blog-Navigation**: Ich hatte damals mal angesprochen _(Anm.: Artikel nicht mehr verfügbar)_, dass mir als Blogleser missfällt, dass ich nicht immer problemlos zurück in die Chronologie eines Blogs einsteigen kann.  
 Am auffälligsten macht sich das meist bemerkbar, wenn man von außen – etwa aus einer Suchmaschine heraus – auf einen einzelnen Blogartikel stößt und nachverfolgen möchte, welche Artikel im ähnlichen Zeitraum veröffentlicht wurden. Man muss sich dann den Titel und/oder das Veröffentlichungsdatum merken und versuchen, das Ding im Archiv ausfindig zu machen. Und dort kann man sich je nach Blogkonfiguration zwar vor und zurück bewegen, jedoch hat man selten (as in: *nie*) die Möglichkeit, an dieser Stelle zeitlich wieder in die Seitenansicht des Blogs einzusteigen. Mit Seitenansicht meine ich diejenige Ansicht, die man vorfände, wenn man von der Startseite aus x Seiten bis zum Artikel zurückgeblättert hätte.

**Nochmal vereinfacht ausgedrückt:** Du kannst im Blog nicht mehr wie in einem Buch lesen, wenn Du von außen eingestiegen bist. Denn die Software zeigt Dir nicht, auf welcher Seite sich der Artikel befindet, den du liest.

---

### Neues WordPress-Plugin: »Entries on page x«

![Screenshot](/content/images/2015/02/entries-on-page-x-link1-250x217.png)

Wir hatten in unserem Blogbeitrag _(Anm.: Artikel nicht mehr verfügbar)_ eine Möglichkeit aufgezeigt, wie man innerhalb eines WordPress-Templates einen Link generieren kann, der zurück auf die Unterseite des Blogs zeigt, auf der der aktuell gelesene Beitrag steht.

Im Zuge der Umstellung dieses Blogs haben wir nun aus der Templatefunktion ein **Plugin** gebaut, um es interessierten Bloggern einfacher zu machen, die Funktionalität ins eigene Blog zu integrieren. Veröffentlicht haben wir es allerdings noch nicht, denn zum einen muss es noch durch die interne Qualitätskontrolle ;), und zum anderen bleiben ein paar konzeptionelle Überlegungen (siehe unten), ob ein derartiges Plugin durchweg taugt und sinnvoll ist.

### Funktionalität des Plugins

Neben der wesentlichen Funktion, die darin besteht, anzuzeigen, auf welcher Unterseite des Blogs der aktuelle Beitrag steht, kann das Plugin noch unterscheiden, welche Art der Auflistung aktiv war: Beiträge nach **Kategorie**, **Schlagwort**, **Datum** oder **Autor** sortiert. Das bedeutet, dass ein Beitrag, der z.B. auf Seite 17 des Blogs steht, innerhalb seiner Kategorie vielleicht nur auf Seite 3 steht. Innerhalb seines Veröffentlichungsmonats vielleicht sogar auf Seite 1.

Was bringt das nun dem Leser, und ist es nicht fürchterlich kompliziert? Ich denke, es ist sehr sinnvoll, und es lässt sich damit irre einfach im Blog navigieren. Siehe die nachfolgende Demonstration.

### Live Demo

~~Wie das Plugin funktioniert, kann man gleich hier im Blog sehen.~~ _(Update: Feature ist nicht mehr aktiv.)_ Der chronologische Link ins Archiv steht ganz oben links über jedem Beitrag. Drei Situationen als Beispiel:

1. **Standard:**  
Rufe den [ersten Artikel](http://blog.decaf.de/2007/04/its-all-about-coffee-benefit/) dieses Blogs auf. Der Link oberhalb des Titels wird etwa so ausschauen (ohne Funktion):  
[**Artikel auf Seite 17**](#)  

2. **Nach Schlagwort:**  
Rufe den gleichen Artikel erneut auf, nachdem du vorher nach dem Schlagwort »[Blogs](/schlagwort/blogs/)« selektiert und bis zum Ende geblättert hast. Der Link wird dann etwa so lauten:  
[**Artikel auf Seite 2**](#) zum Schlagwort »**Blogs**«  

3. **Nach Datum:**  
Durchblättere alle Artikel des Monats [April 2007](/2007/04/) und wähle erneut den ersten Artikel dieses Blogs aus. Der Link wird sein:  
[**Artikel auf Seite 2**](#) im **April 2007**

*(Ausführliche technische Hinweise bringe ich im nächsten Beitrag zum Thema oder spätestens bei Veröffentlichung des Plugins an, sonst wird es an dieser Stelle zu umfangreich. Ganz kurz nur: Sollte ein anderer als der WordPress-eigene Caching-Mechanismus aktiv sein, liefert das Plugin immer nur den schlichten Standardlink ohne Kategorie, Schlagwort, Datum oder Autor. Gleiches gilt für den Fall, dass Cookies deaktiviert sind.)*

---

### Konzeptionelle Überlegungen, Test und Feedback

Konzeptionell bin ich mir noch unsicher, ob die oben beschriebene Methode durchweg sinnvoll ist, oder ob es Situationen oder Blogumgebungen gibt, in denen eine Navigation in der Form nicht funktioniert. Mir kommen dabei magazinartige Blogs in den Sinn, die ihre Artikel vielleicht nach einem Schema ausgeben, das wenig linear oder nachvollziehbar ist, etwa Kategorie mit Tag oder Datum gemischt. Oder auch Multiautoren-Blogs, die ihre Beiträge nach ungewöhnlichen Kriterien vermischen.

Vermutlich hilft nur ein Testen mit möglichst vielen verschiedenartigen Blogs. Wer Interesse hat, mag sich gerne mit gültiger E-Mail-Adresse in den Kommentaren melden!

Und natürlich gilt:  
**Diskussion zum Thema** ist erwünscht und wird dankend angenommen :)

---

### Nachtrag: Plugin veröffentlicht

Das Plugin wurde inzwischen veröffentlicht, siehe [Entries on page x](http://blog.decaf.de/2008/12/entries-on-page-x/).


