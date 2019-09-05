---
layout: post
title: "REDAXO mit Docker \U0001F433"
featured: true
image: "/content/images/2017/07/redaxo-demo-base.png"
date: '2017-07-09 16:33:05'
tags:
- redaxo
- note
---

Falls ihr schon immer [REDAXO](https://redaxo.org) testen wolltet, bisher aber keine Zeit oder Lust hattet, eine Entwicklungsumgebung einzurichten, das Setup zu durchlaufen und eine Demo zu installieren, könnt ihr mal unser __Docker-Setup__ benutzen, das wir neulich bei [Friends Of REDAXO](https://github.com/FriendsOfREDAXO/redaxo-mit-docker) veröffentlicht haben.

Das Paket ist sehr ausführlich dokumentiert und soll vor allem auch eine __Hilfe für Einsteiger\_innen__ 🚀 sein, die noch keine Docker-Erfahrung mitbringen. Mit ganz wenig Aufwand habt ihr am Ende eine schicke Entwicklungsumgebung mit einem lauffähigen REDAXO CMS, das eine umfangreiche Website-Demo implementiert hat:

<img style="outline: 0;" src="/content/images/2017/07/redaxo-demo-base.png" alt="Screenshot der REDAXO-Basisdemo">

Das Paket eignet sich also für Leute, die mit __Docker__ rumspielen wollen, und für Leute, die mit __REDAXO__ rumspielen wollen. Wer beides will, bekommt den Jackpot! 🎉

---

### Kurzanleitung in 3 Schritten

1. Installiere [Docker für dein System](https://www.docker.com/community-edition#/download).  
Falls du Windows 7 benutzt, brauchst du die Docker Toolbox. In der Docker-Konfiguration musst du die Ordner freigeben, mit denen Docker arbeiten darf.
2. Benutze `docker-compose up -d`.  
Damit wird Zeug aus dem Netz geladen und ein Haufen Text durch deine Konsole laufen. Wenn der Eingabe-Prompt wieder erscheint, wurden deine Docker-Container gestartet, jedoch ist REDAXO noch nicht fertig. Warte einfach noch 1-2 Minuten…
3. REDAXO ist im Browser erreichbar unter `http://localhost:20080`.  
In den REDAXO-Adminbereich kommst du über `http://localhost:20080/redaxo` mit den Logindaten `admin`/`admin`.
 
---

### Infos und Hilfe

Ausführliche Informationen erhälst du auf der Projektseite: https://github.com/FriendsOfREDAXO/redaxo-mit-docker

Falls du Hilfe brauchst, Fragen hast oder allgemein an REDAXO interessiert bist, besuche am besten den Slack-Chat. Eine Einladung zum Slack bekommst du hier: https://redaxo.org/slack/