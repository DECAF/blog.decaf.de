---
layout: post
title: 'Blog-Navigation: Paging (2)'
description: "Weblogs sind Ringordner. Wir blättern »ältere Beiträge« nach rechts/unten weiter und »neuere Beiträge« nach links/oben zurück."
author: ds
more: true
---

*Dieser Artikel ist eine Ergänzung zum Thema Blog-Navigation. Der letzte Artikel über [Paging](http://blog.decaf.de/2008/01/blog-navigation-paging) in Weblogs wolle eine gängige Seiten-Navigation verbessern, die man häufig auch auf anderen Websites zu sehen bekommt, und die vom Benutzer recht intuitiv verstanden wird, wenn sie geschickt eingesetzt wird.*

Viele Blogs beschränken sich statt der kompletten Pagination auf die beiden **Links zum vor- und zurückblättern einer Seite** (Ich nenne sie gerne schlicht »Blättern-Links«). Eigentlich gibt es dabei aus konzeptioneller Sicht nicht viel zu beachten, und dennoch scheinen sich bisher keine Konventionen oder *Best Practices* gebildet zu haben, wie ein Blog funktionieren soll. Es herrscht Wildwuchs.

Bei den »Blättern-Links« gilt es drei Dinge zu beachten:

1. **Die Laufrichtung**  
 (welcher von beiden zeigt nach links, welcher nach rechts?)
2. **Die Positionierung**  
 (welcher von beiden steht links, welcher rechts?)
3. **Die Benennung**  
 (»weiter« und »zurück«?)

Ich möchte gerne meine persönliche Vorstellung davon beschreiben, wie die Navigation funktionieren sollte. Ein *richtig* und *falsch* gibt es dabei sicherlich nicht, denn Webnutzer sind selten schwarz-weiß.

### Chronologie vs. Lesegewohnheiten

Als Benutzer grafischer Interfaces (»GUIs«) sollte man eine Sache verinnerlicht haben: nach links geht es in der Regel zurück/rückwärts, nach rechts geht es weiter/vorwärts. Je nach Art der Anwendung kann es auch oben und unten sein. Der Ursprung dafür ist unsere Leserichtung: wir lesen von links nach rechts und von oben nach unten. Wollen wir also vorankommen, gehen wir weiter in Leserichtung nach rechts/unten, und wollen wir zurückgehen, gehen wir entgegen der Leserichtung nach links/oben. Im Buch blättern wir nach rechts weiter und nach links zurück.

Die **Chronologie** eines Weblogs sorgt an dieser Stelle allerdings für Verwirrung. Im Blog stehen neuere Beiträge vorne, ältere hinten. Ausgehend von Seite 1 muss der Leser also chronologisch *zurück*blättern, während er rein technisch gesehen *weiter*liest. Das hat Konfliktpotential, denn während die eine Gruppe von Blogautoren an den Lesegewohnheiten hängt und ihre Besucher nach rechts auf die nächste Seite schickt, ist für die andere Gruppe die Chronologie des Blogs so wichtig, dass ihr Link auf die nächste Seite stattdessen nach links – also zurück – zeigt (So macht es übrigens auch das vermutlich noch immer am weitesten verbreitetste WordPress-Template »Kubrik«).  
 Dabei wird auch gerne die **Symbolik des Buchs** herangezogen und auf Blogs gemünzt: demnach befindet sich der Leser auf der Startseite des Blogs bereits am Ende des Buchs, dort, wo nach und nach weiter geschrieben wird. Und will er von dort aus weiterlesen, muss er zurückblättern: chronologisch und technisch.

Spätestens an dieser Stelle geht alles durcheinander. Kaum ein Leser wird Verständnis für die Symbolik haben, sich beim Betreten einer Website bereits auf der letzten Seite eines Buchs zu befinden. Selbst wenn man es ihm erklärte, ihm zudem bewusst sein sollte, dass es sich bei der Website um ein Blog handelt und dass Bloginhalte umgekehrt chronologisch ausgegeben werden: die letzte Seite ist einfach zu weit hergeholt.  
 Und wenn man es genau nehmen möchte, wäre auch die Navigation nicht konsistent, denn nach der Buchsymbolik müsste *über* dieser (ersten Blogseite) letzten Buchseite bereits ein Link zum Zurückblättern und die Seitenzahl X stehen, um die aktuelle Leseposition zu beschreiben. Das habe ich noch in keinem Blog in der Form auf der ersten Seite gesehen.

Die Buchsymbolik haut aber durchaus hin, auch für Weblogs. Man muss lediglich eine **andere Form von Büchern** verwenden:

### Das Weblog als Ringordner

Neue Beiträge werden ganz einfach vorne eingehängt. Bei jeder Veröffentlichung wird dem Buch also ein Blatt hinzugefügt. Keine große Erkenntnis *(Update: [vor allem keine neue](http://www.peterkroener.de/2008/01/12/weblog-navigation-vor-oder-zurueck/#comment-6381))*, jedoch ist damit endlich der Navigationskonflikt aus der Welt geräumt: weitergeblättert wird nach rechts, zurück nach links. Sorgt man jetzt noch für eine ordentliche Benennung der Links, sollte die Navigation intuitiv verständlich sein: »ältere Beiträge« und »neuere Beiträge« statt vor, zurück oder irgendwas.

Und um gleich das Argument zu entschärfen, dass beim Ringbuch nach jeder Veröffentlichung eines neuen Beitrags sämtliche Seitenzahlen wegradiert und neugeschrieben werden müssten: vollkommen richtig, so ist es auch. Im Internet übernimmt diesen Part allerdings die Blogsoftware.

### Persönliches Fazit

Weblogs sind Ringordner. Wir blättern »**ältere Beiträge**« nach rechts/unten weiter und »**neuere Beiträge**« nach links/oben zurück.

(Und weil es »persönliches Fazit« heißt: die Aussage ist nicht in Stein gemeißelt, sondern lediglich Diskussionsgrundlage..)

---

### Weitere Artikel zum Thema

- [Blog-Navigation: Paging](http://blog.decaf.de/2008/01/blog-navigation-paging)
- ~~[Blog-Navigation: Der »Artikel auf Seite x«-Link](http://blog.decaf.de/2007/04/blog-navigation-the-entries-on-page-x-link)~~

#### Artikel auf anderen Websites

- [Weblog-Navigation: Vor oder zurück?](http://www.peterkroener.de/2008/01/12/weblog-navigation-vor-oder-zurueck/) (Peter Kröner)
- [Seitennavigation in Weblogs](http://tordox.org/23/seitennavigation-in-weblogs) (tordox.org)
- [Usability von Seiten-Navigationen](http://aktuell.de.selfhtml.org/weblog/seitennavigation) (Mathias Schäfer)


