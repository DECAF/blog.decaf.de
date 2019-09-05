---
layout: post
title: "»Reset Reloaded«: Browserstyles zurücksetzen"
description:
author: ds
categories: []
---

Browser tragen bekanntlich ein **internes Basisstylesheet** mit sich rum, das auf jedes Dokument angewendet wird, um eine Grundstruktur zu erreichen. Das ist sinnvoll und sorgt dafür, dass auch Dokumente ohne ein eigenes Stylesheet strukturiert sind: Überschriften werden hervorgehoben, Textabsätze haben einen Abstand nach unten, Listen werden eingerückt, etc.

Bei der Umsetzung von Websites geraten Webautoren jedoch gerne mal in **Konflikt mit den Basisstyles** des Browsers, wenn sie es verpassen, die Browservorgaben durch eigene Angaben zu überschreiben. Das, was bei der Kontrolle auf dem eigenen System dann wie gewollt aussieht, kann beim Nutzer unter anderen Bedingungen verfälscht werden. Ein typisches – wenn auch seltenes – Beispiel dafür ist, dass verpasst wird, eine Hintergrundfarbe für den `body` zu definieren, weil der Webautor von einem weißen Hintergrund ausgeht. Im Regelfall wird der Benutzer dann auch einen weißen Hintergrund erhalten, weil es die Standardvorgabe nahezu jedes Browsers ist, jedoch lässt sich der Farbwert meistens in den Browsereinstellungen verändern, so dass es durchaus vorkommen kann, dass aus Weiß ein freundliches Pink oder ein himmelblaues Grün wird.

Aus Sicht des Webautors kann es deshalb sinnvoll sein, Browservorgaben zu Beginn seiner Stylesheets **zurückzusetzen**, um danach unter (hoffentlich) gleichen Bedingungen für alle Browser/Systeme individuelle Werte einzusetzen.

Aber wie so oft: die Betonung liegt auf *»es **kann** sinnvoll«* sein. Denn im Gegenzug zu der Situation, es ohne ein vorheriges Zurücksetzen der Browserstyles zu verpassen, bestimmte Vorgaben mit eigenen Styles zu überschreiben und damit u.U. ungewollte Ergebnisse hervorzurufen, kann es bei der eben erwähnten Methode des Zurücksetzens passieren, dass verpasst wird, allen Elementen einen **neuen Style** zuzuweisen. Der Browser würde dann mit »Nullwerten« für diejenigen Elemente arbeiten, die nicht explizit vom Webautor angefasst wurden, und das kann z.B. dann zum Problem werden, wenn während der Entwicklung der Website noch nicht bekannt ist, welche Inhalte samt ihrer Elemente zur Auszeichnung später verwendet werden.

Wer als Webautor also konsequent alle Browserstyles zurücksetzt, müsste danach im Gegenzug genauso konsequent alle (vorkommenden) Elemente neu definieren, um keine Überraschungen zu erleben, wenn auf der Website neue Inhalte eingebracht werden — etwa vom Redakteur innerhalb des Content Management Systems oder vom Leser eines Blogs, der einen Kommentar hinterlässt.

Ich selbst bin eher kritisch gegenüber dem Reset, also dem Zurücksetzen der Browserstyles, und arbeite lieber mit der Umgebung, die mir vom Browser zur Verfügung gestellt wird. Die Styleangaben, die ich als Webautor verwende, sind aus dieser Sicht heraus lediglich ergänzende Styles. Aber natürlich sollten sie detailiert genug sein, um ein Ausgabeergebnis zu erhalten, das den Anforderungen entspricht und im Wesentlichen systemübergreifend einheitlich ist.

Nach langem Gerede nun noch der nützliche Hinweis an alle diejenigen Webautoren, die nach der Erstmal-alles-Zurücksetzen-Methode arbeiten: **Eric Meyer** hat heute seine vermutlich finale Variante vorgestellt, diese Aufgabe zu erledigen:

> I have what I’m willing to call the final version of my take on the topic of reset styles.
> 
> - Eric Meyer, [**Reset Reloaded**](http://meyerweb.com/eric/thoughts/2007/05/01/reset-reloaded/)

Der IE/Win benötigt dabei wie üblich eine Sonderbehandlung, auf dessen verschiedene Ansätze Eric ebenfalls hinweist, sie jedoch als nicht zwingend notwendig betrachtet.

Und abschließend noch zu Formularelementen, die vom Reset bisher nicht erfasst sind:

> I’m going to get to that “weirdness of form elements” post in the near future.

After my troublesome approach of achieving [consistent flexible forms](http://blog.decaf.de/2007/04/approach-to-flexible-multicolumn-forms/): I’m looking forward to it, Eric! Maybe there will be some things to improve.

---

### Weitere Artikel zum Thema

1. [**YUI Reset CSS**](http://developer.yahoo.com/yui/reset/)  
Yahoo!s Methode, Browserstyles zurückzusetzen, auf der Meyers Ansatz basiert ursprünglich basierte, siehe [Reset Styles](http://meyerweb.com/eric/thoughts/2007/04/12/reset-styles/).
2. [**Undoing html.css and using debug scaffolding**](http://tantek.com/log/2004/09.html#d06t2354)  
Tantek Çeliks Ansatz eines Resets.
3. [**YAMLs Basis-Stylesheet base.css**](http://yaml.de/artikel/css/base.html) (Dirk Jesse)

*(Der Artikel wurde parallel auch im [SELFHTML-Blog](http://aktuell.de.selfhtml.org/weblog/browserstyles-zuruecksetzen-reset-css) veröffentlicht.)*


