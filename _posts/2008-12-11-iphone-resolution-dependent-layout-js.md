---
layout: post
title: "iPhone + Resolution dependent layout (JS)"
description:
author: ds
---


![decaf-iphone](/content/images/2015/02/decaf-iphone.jpg)

Das iPhone ist so geschickt im Umgang mit dem *echten* Web, dass unsere Website und das Blog in ihrer Struktur bereits ohne spezifische Anpassungsarbeiten recht gut angenommen wurden. Unsere Inhalte müssen (noch) nicht unbedingt mobil sein, deshalb hätte uns der Status Quo längst ausgereicht. Allerdings gab es eine kleine Anpassung zu machen, die in diesem Fall einen angenehmen zweiten Effekt hinterher gezogen hat:

### Viewport-Breite im mobilen Safari

`<code allow="none"><meta content="width=641" name="viewport"></meta>`

(Siehe [Safari HTML Reference](http://developer.apple.com/documentation/appleapplications/reference/safarihtmlref/Articles/HTMLExtensions.html#//apple_ref/doc/uid/TP40002066-DontLinkElementID_13))

Diese Angabe betrifft den mobilen Safari und schrumpft dessen Viewport auf 641 Pixel in der Breite, was wiederum dazu führt, dass die Methode **»[Resolution dependent layout](http://www.themaninblue.com/experiment/ResolutionLayout/)« des Man in Blue** per [Event Listener](http://www.mediaevent.de/javascript/event_listener.html) zuckt und dem body eine CSS-Klasse vergibt, die wir in unseren Stylesheets für kleine Screens verwenden.  
 Das iPhone nimmt danach diese 641 Pixel breite Website und schrumpft sie auf 320 Pixel im Hochformat oder 480 Pixel im Querformat, je nachdem, wie man das Gerät hält.

Das Ergebnis sieht man in den Screenshots oben. Well done, dieser Zustand reicht uns nun *wirklich* für ein mobiles Web auf dem iPhone/iPod aus. Kein Bedarf, z.B. die etwas klein geratene Navigation anzupassen oder weiteres Feintuning zu machen.

---

### Fazit?

Die Empfehlung für alle, die die **Resolution-Methode des Man in Blue** einsetzen — sehr sinnvoll übrigens, wir verwenden sie in vielen unserer Projekte als Alternative zu flüssigen Layouts — und kein Interesse daran haben, ihre Websites mit spezifischen Styles fürs iPhone zu versehen, mag also sein: Schaut mal, ob ihr über die Viewport-Breitenangabe nicht einen geschickteren Zoom erreichen könnt. Es ist nur eine Zeile im HTML, die iPhone-Nutzer glücklich machen kann.

### Link: iPhone-FAQ

Wer an dieser Stelle weiter machen möchte und noch einen geeigneten Einstieg braucht, mag einen Blick auf Timos und Stephans Artikel **»[FAQ: Websites für das iPhone gestalten](http://www.vorsprungdurchwebstandards.de/theory/faq-websites-fuer-das-iphone-gestalten/)«** werfen.


