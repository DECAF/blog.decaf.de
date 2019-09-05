---
layout: post
title: Kurzes URL-Schema in REDAXO
image: "/content/images/2015/02/shorturl.png"
date: '2009-05-06 18:36:27'
tags:
- redaxo
---


![shorturl](/content/images/2015/02/shorturl.png)

In Zeiten von Twitter und Aufmerksamkeitsdefiziten kann es wieder reizvoll sein, sehr kurze URLs zu verwenden. Statt `www.meine-domain.tld/bereich/oberkategorie/unterkategorie/noch-irgendwas/und-dann/meine-seite/` also ein schlichtes  
```
www.meine-domain.tld/meine-seite/
```

Suchmaschinenzeroptimierer mögen jetzt hektisch wedeln, ist doch die URL viel zu wertvoll, um sie dermaßen zu kappen. Wer jedoch fokussieren möchte – auf Menschen und Inhalte – darf sich gerne kurz halten.

Hier ist eine Möglichkeit zur Verwendung des kurzen URL-Schemas im Content-Management-System [REDAXO](http://redaxo.de) (ab Version 4.2) und des hauseigenen Addons **url_rewrite**:

### Kurzes URL-Schema in REDAXO

![redaxo](/content/images/2015/02/redaxo.png)

**Download der angepassten Rewrite-Klasse:**  

_(Update: Nicht mehr aktuell. Benutzt besser das Addon SEO42.)_

- ~~für REDAXO 4.2: [class.rewrite_fullnames_onelevel.zip](http://decaf.de/articles/short-urls-in-redaxo/r4.2/class.rewrite_fullnames_onelevel.zip)~~ 
- ~~für REDAXO 4.3: [class.rewrite_fullnames_onelevel.zip](http://decaf.de/articles/short-urls-in-redaxo/r4.3/class.rewrite_fullnames_onelevel.zip)~~

**Anleitung:**

1. Das url_rewrite-Addon aktivieren und einrichten. (Bitte die Installationshinweise im Addon beachten!)
2. Die **angepasste Rewrite-Klasse** runterladen und ins Addon-Verzeichnis kopieren nach `/redaxo/include/addons/url_rewrite/classes/`
3. In der Konfigurationsdatei des Addons `config.inc.php` in Zeile 25 die neue Rewrite-Klasse einsetzen.
4. Im Administrationsbereich von REDAXO unter *System > Einstellungen* den Cache löschen, damit die Änderungen wirksam werden.

**Bitte beachten:**

- Die Verwendung dieses Schemas ist nur dann sinnvoll, wenn sicher gestellt werden kann, dass **keine zwei gleichlautenden Artikel oder Kategorien** existieren, die beim Rewrite die gleiche URL ergäben!
- Die neue Rewrite-Klasse sorgt zusätzlich dafür, dass **Leerzeichen innerhalb der URL** nicht durch ein `+` ersetzt werden (seit REDAXO 4.2) sondern wie in zuvor durch ein `-` (bis REDAXO 4.1). Wer das nicht möchte, kann Zeile 339 auskommentieren, siehe Hinweis innerhalb der Datei.  
*(Ab REX 4.3 nicht mehr nötig, da per default wieder `-` verwendet werden.)*
- **Update 18.01.2010:** Bei Mehrsprachigkeit: a) Alle Startartikel erhalten Sprachkürzel-URL (Bsp.: `domain.tld/de/` statt `domain.tld/de/startseite/`), b) Der Startartikel der Hauptsprache (clang 0) erhält Basis-URL OHNE Sprachkürzel (Bsp.: `domain.tld` statt `domain.tld/de/`).  
 Bugfix: `$REX['NOTFOUND_ARTICLE_ID']` kam immer in clang 0.
- **Update 27.05.2010:** Anpassung für REDAXO 4.3

---

## Diskussion im REDAXO-Forum

Die Kommentare sind in diesem Beitrag geschlossen. Zur Diskussion bitte das REDAXO-Forum benutzen, vielen Dank!  
[http://forum.redaxo.de/sutra67784.html](http://forum.redaxo.de/sutra67784.html)


