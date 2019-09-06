---
layout: post
title: 'Ghost: Wie erstellt man eine sitemap.xml?'
description:
author: ds
---

> There's an app for that.

Nein, es gibt keine App (Plugins heißen bei Ghost Apps), die Sitemaps erstellt. Es gibt aktuell noch gar keine Apps in Ghost. Apps sind das _most wanted feature_ für die kommenden Releases.

Wie also generiert man eine `sitemap.xml`?  
Gar nicht. Ghost macht das nämlich klammheimlich selbst. Das [Feature](https://github.com/TryGhost/Ghost/pull/4348) ist in den letzten Releases mit eingeflossen, ohne dass es allzu groß kommuniziert wurde. Wer davon nichts mitbekommen hat, wird es auch nicht ohne weiteres bemerken, denn die Sitemaps (es sind mehrere) werden nicht wie üblich als Ressource auf dem Server abgelegt, sondern vorerst noch dynamisch generiert.

Unsere schaut so aus:

![sitemap.xml](/content/images/2015/02/sitemap-xml_01.png)

Es gibt Listen von __Pages, Posts, Autor_innen und Tags__.

Mit der `sitemap-posts.xml` hat man also ein vollständiges Inhaltsverzeichnis – nativ in jedem aktuellen Ghost-Blog implementiert – vorliegen:

![sitemap-posts.xml](/content/images/2015/02/sitemap-xml_02.png)

> Awesome.

<small>P.S.: Wer sich über die eigenartigen Post-Titel in unserer Sitemap wundert, die nur aus langen Zahlen bestehen: Das sind Twitter-Posts. Manches von dem, was wir bei Twitter posten, landet zukünftig auch hier im Blog. Zu dem Thema schreibe ich gerne demnächst mal ausführlicher, falls es jemanden interessiert.</small>

