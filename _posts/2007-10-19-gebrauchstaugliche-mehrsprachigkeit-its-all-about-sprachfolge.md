---
layout: post
title: 'Gebrauchstaugliche Mehrsprachigkeit: it’s all about Sprachfolge'
description: "Mehrsprachigkeit ist gar nicht einfach. Aber wenn wir schonmal dabei sind, sollten wir drei Maßnahmen beachten."
author: ds
more: true
---

Mehrsprachige Websites zu entwickeln scheint im ersten Moment recht einfach: man spiegelt die vorhandene Struktur und den Content, done. Wer’s genau nimmt, macht sich noch Gedanken über URL-Schemata und die Sprachauswahl (automatisch und manuell), interne Verlinkung oder eine mögliche Mehrfachverwertung von Inhalten. Und diejenigen, die es sehr genau nehmen, fangen nicht eher mit der Umsetzung an, bevor nicht das Wort »[**Content Negotiation**](http://de.wikipedia.org/wiki/Content_Negotiation)« gefallen ist.

Letzterer ist der Punkt, der von den eben genannten am meisten auf die **Gebrauchstauglichkeit** der Website abzielt. Content Negotiation ist die Möglichkeit, dass ein *Jaap* einem *Pierre* einen Link von www.example.be schicken kann, und dass *Pierre* mit diesem Link die *französische* Variante der Website aufruft, während *Jaap* doch die *flämische* Version der Seite gelesen hatte — so erklärt man es beim [W3C](http://www.w3.org/International/questions/qa-when-lang-neg). Gebrauchstauglichkeit deshalb, weil die Ausgabe des Inhalts sich nach der im Browser angegebenen Sprachfolge von Jaap und Pierre richtet, ohne dass die Jungs dafür irgendwas auf der Website angeklicken müssen (wobei sie natürlich auch manuell die Sprache wechseln können).

It’s all about Sprachfolge, und das macht’s im Backend ein Stück weit komplizierter als anfangs noch angenommen. Neben den technischen Fragen sollte man auch über *konzeptionelle* Fragen nachdenken, etwa: was bekommen Nutzer zu sehen, die wichtige Einstellungsmöglichkeiten ihres Browsers zurecht nicht auf der vierten Ebene eines unscheinbaren Menüs vermuten, und dessen Firefox deshalb ausschließlich Englisch spricht? Und wie läuft das eigentlich für mich als Anbieter mit Fotos und anderen Medieninhalten auf meiner Website: muss ich nun jedes Bild in allen Sprachen einstellen und klicke mich in Bildergalerien noch um den Verstand?

Nein, Mehrsprachigkeit ist nicht einfach. Aber wenn wir schonmal dabei sind, sollten wir drei Maßnahmen beachten:

### 3x Mehrsprachigkeit mit Gebrauchstauglichkeit, bitte! Zum Mitnehmen.

`1.` **Eine sinnvolle Sprachfolge**

Die Inhalte der Website sollten natürlich zuerst in der primären Landessprache des Nutzers erscheinen. Ist der Inhalt einer Seite jedoch nicht in dieser Sprache verfügbar, wird auf die nächste Sprache zugegriffen, die der Nutzer – falls er denn mehrere Sprachen spricht – hoffentlich in seinem Browser angegeben hat.

Diese Sprachfolge sollte sich nicht nur auf ganze Seiten innerhalb des Webangebots beziehen, sondern kann auch **einzelne Inhaltsbereiche** betreffen. So kann es in der Praxis zum Beispiel vorkommen, dass ein neues Produkt in den Onlinekatalog des Unternehmens aufgenommen wird, ohne dass zu diesem Zeitpunkt schon alle Übersetzungen verfügbar sind. In diesem Fall ist es sinnvoll, dass *Jaap*, der Fläme, nicht etwa alles auf Englisch sieht, sondern dass die Navigation und alle begleitenden Inhalte in Flämisch ausgegeben werden, während nur der innere Teil der Produktansicht, für den noch keine Übersetzungen verfügbar sind, auf Englisch ausgegeben wird. An dieser Stelle wird der nachfolgende Punkt besonders wichtig:

`2.` **Ein Hinweis auf fehlende Inhalte in der ausgewählten Landessprache**

Ist ein Inhalt nicht in der Landessprache des Benutzers vorhanden, sollte dieser einen Hinweis darauf – natürlich in seiner Landessprache formuliert – bekommen. Als freundlicher Inhaltsanbieter könnte man dem Nutzer bei der Gelegenheit auch gleich mitteilen, an wen er sich mit dringenden Fragen wenden kann, um eine Übersetzung zu erhalten.

Wichtig also: fehlende Inhalte in einer Sprachversion müssen markiert werden.

`3.` **Inhalte im Backend direkt für alle Sprachen übernehmen**

Gebrauchstauglichkeit nicht nur für den Nutzer, sondern auch für den Anbieter: Beim Einpflegen von Inhalten kann man ihm viele Schritte abnehmen, wenn man Inhalte, die für alle Sprachen in gleicher Form gelten, von Anfang an verfügbar macht und für alle Sprachen übernimmt. Das betrifft z.B. das Bildmaterial, Links/URLS, verknüpfte Download-Ressourcen, Kontaktdaten, etc. – Vielleicht gibt das CMS von Haus aus bereits alle Inhalte vor, um sie 1:1 lesen und übersetzen zu können – prima. In allen anderen Fällen – und die werden in unserer Gegend der kleinen und <del>feinen</del> freien CMS überwiegen – sollte man es nicht allein dem Redakteur überlassen, die Inhalte vollständig und in richtiger Reihenfolge erfassen zu müssen, sondern man kann ihm einen Haufen Arbeit dadurch abnehmen, dass man ihm bekannte Strukturen und Inhalte schon vorgibt, um die er *drumrum* schreiben kann.

Davon profitiert letztendlich wieder der Nutzer, auch wenn er das wohl niemals erfahren wird.


