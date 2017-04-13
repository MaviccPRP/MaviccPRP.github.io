---
title: 'CSS und JQuery - Ein eigenes Dropdown-Menü'
date: 2013-06-12T13:38:02+00:00
author: Phillip Richter
layout: post
permalink: /mit-css-und-jquery-zum-horizontalen-menu/
categories: CSS
---
<iframe src="http://www.youtube.com/embed/rOcjdZ3uBsg" height="315" width="560" allowfullscreen="" frameborder="0"></iframe>

Heute folgt quasi eine Fortsetzung des CSS-Tutorials &#8222;horizontales Menü erstellen&#8220; von letzter Woche. Mithilfe von JQuery erweitern wir das horizontale Navigationsmenü mit einer Dropdown-Funktion. Dadurch wird es möglich Untermenüs in unser vorhandenes Menü einzufügen, die bei Bewegung der Maus über einen Navigationseintrag eingeblendet werden.

<!--more-->

Um die Funktionalität von JQuery auf der eigenen Seite nutzen zu können, muss man JQuery in seinem HTML Dokument integrieren. Am besten geschieht dies, indem man folgende Zeile in den Header Bereich des Dokuments einfügt:****

<code class="snippet">&lt;script src="//ajax.googleapis.com/ajax/libs/jquery/1.10.1/jquery.min.js"&gt;&lt;/script&gt;</code>

Hierbei nutzt ihr die Google-API, die es erlaubt die Javascript Bibliothek JQuery extern auf eure Seite zu laden. Dadurch muss man nicht mehr die Bibliothek auf den eigenen Server hochladen. Dies kann man alternativ natürlich ebenfalls tun, das würde dann etwa so aussehen:

`<script src="js/jquery.min.js"></script>`

Dieser Code setzt voraus, dass die minifizierte JQuery Datei im &#8218;js&#8216; Verzeichnis eures Webservers installiert ist. Ist die Javascript-Bibliothek erst einmal geladen, kann man damit zahlreiche schöne Effekte realisieren. In diesem Tutorial könnt Ihr euch nun ansehen, wie JQuery einen Dropdown Effekt erzeugen kann.

Das Styling der Navigationsleiste beruht weiterhin auf CSS, wobei ich für die horizontale Darstellung dieses Navigationsmenüs den CSS-Befehl &#8218;float&#8216; genutzt habe. Für weitere Informationen dieses sehr nützlichen CSS Features empfehle ich euch folgende Tutorials:

Eine eher theoretische, aber äußerst nützliche Einführung bietet <a title="CSS float" href="https://www.youtube.com/watch?v=IiJzbXzOdHQ" target="_blank">Christopher Stein in seinem Video-Tutoria</a>l.

Flame Div gibt in <a title="CSS float" href="https://www.youtube.com/watch?v=Kkh7Yt5LCfQ" target="_blank">seinem Tutorial</a> einen praktischen Einstieg in der Arbeit mit &#8218;float&#8216;,
