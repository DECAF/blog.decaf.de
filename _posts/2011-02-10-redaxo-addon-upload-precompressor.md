---
layout: post
title: 'REDAXO-Addon: Upload Precompressor'
description:
author: ds
---


**Kurzbeschreibung:** Das Addon verkleinert übergroße Bilder (JPG) nach Upload in den Medienpool auf eine festgelegte Maximalgröße. Bereits vorhandene Bilder können zudem nachträglich verkleinert werden.

![Upload Precompressor](/content/images/2015/02/upload_precompressor_01.png)

### Beschreibung

[REDAXO](http://www.redaxo.org) verfügt über Funktionen zur **dynamischen Bildgenerierung** auf Basis der [GDlib](http://de.wikipedia.org/wiki/GD_Library). Das klappt prima, hat aber technische Grenzen: Das Erzeugen eines Thumbnails aus einem Original-Bild mit 2000px Breite und Höhe kann etwa 19 MB RAM benötigen (bei CMYK 40 bit, was natürlich recht doof ist). Ist das Bild 3000px groß, braucht es schon bis zu 43 MB RAM. Hinzu kommt ein Mehrverbrauch von CPU-Kraft, viel unnötiger Platz auf dem Webserver für all diese großen Bilder und nicht zuletzt eine schlechte Performance beim Erstaufruf der Website.

Übergroße Bilder im Medienpool sollten also vermieden werden, sie gehen zu Lasten der **Ressourcen**. Aber was passiert, wenn die Inhaltspflege der Website an Redakteure/Kunden über geht? Ihnen fehlen oftmals die Werkzeuge und/oder die Erfahrung im Umgang mit Bildmaterial, so dass die Bilder gerne auch mal direkt von der Digitalkamera ins CMS wandern.

Hier möchte das Addon [Upload Precompressor](http://www.redaxo.org/de/download/addons/?addon_id=839) ansetzen. Es verkleinert Bilder nach Upload in den Medienpool auf eine festgelegte Größe, die sinnvoll für das CMS ist. Das könnten etwa 1500px oder auch nur 1000px sein. Mit diesen kann REDAXOs Bildprozessor dann geschickter hantieren als mit den übergroßen Originalen. Letztere werden verworfen, so dass mehr Platz auf dem Server bleibt. Zudem kann ein Nutzer mit Admin-Rechten den Batch-Prozess des Addons anwerfen, der nachträglich alle großen Bilder einer bestehenden Website schrumpft.

### Details

Noch ein paar Worte zur Anwendung: Das Addon selbst benötigt natürlich ebenso wie der REDAXO-eigene Bildprozessor haufenweise Ressourcen, um große Bilder zu bearbeiten. Aus dem Grund ist es nicht sinnvoll, das Addon in wenig leistungsstarken Shared-Host-Umgebungen einzusetzen. Es werden mindestens **32 MB RAM** benötigt, andernfalls lässt sich das Addon gar nicht erst installieren. 64 MB sind besser, damit sollte es im Alltag hoffentlich flüssig laufen.

Der Batch-Prozess des Addons arbeitet die betreffenden Bilder einzelnd von klein nach groß (betrifft Pixel, nicht Dateigröße) ab. Wenn unterwegs der Speicher voll läuft, wurden zumindest alle Bilder durchgezogen, die unter dem Grenzwert des Scheiterns lagen. In diesem Fall hilft nichts weiter, als dem Webpaket mehr RAM zu spendieren, oder aber die übrig gebliebenen Bilder von Hand zu schrumpfen.

Zum Schluss: Läuft der Speicher voll, bleibt kein Ausweg. Der Prozess stoppt, je nach Serverkonfiguration wortlos oder mit einem **fatal error**. Das Addon kann so etwas leider nicht prüfen oder abfangen. Immerhin geschieht der Abbruch in einem iFrame, so dass nicht die gesamte Seite abstürzt und weiß wird.

Und: Keine Gewähr oder sowas. Das Ding vergreift sich an Euren Bildern, ihr solltet besser vorher ein **Backup** machen!

---

### Links:

- [Upload Precompressor im REDAXO-Addonverzeichnis](http://www.redaxo.org/de/download/addons/?addon_id=839)
- [Diskussion im REDAXO-Forum](http://www.redaxo.org/de/forum/addons-f30/upload-precompressor-t16257.html)
