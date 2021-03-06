---
id: 212
title: Float und Clear – Positionieren mit CSS
date: 2013-06-26T12:52:33+00:00
author: Phillip Richter
layout: post
guid: http://bestinnovations.de//?p=212
permalink: /float-und-clear-richtig-positionieren-mit-css/
categories:
  - CSS
redirect_from: "/wordpress/float-und-clear-richtig-positionieren-mit-css/"
---
**Eines der größten Hürden für den Einstieg in CSS ist sicherlich die Positionierung. Diese ist in CSS nicht immer ganz intuitiv und erfordert einen nicht zu unterschätzenden Lernaufwand. Mit diesem kleinen Tutorial möchte ich die CSS Befehle _float_ und _clear_ näher erläutern und zeigen wie man mit diesen Werkzeugen richtig umgeht.**
  
<!--more-->

## Das HTML-Grundgerüst

Zunächst bauen wir eine kleine HTML-Seite, in der es einen Hauptcontainer gibt, der wiederum vier DIV-Container enthält. Dabei könnte man sich vorstellen, dass der Hauptcontainer der Hintergrund ist und die vier DIV-Containern Textbeiträge oder Bilder enthalten. Doch beginnen wir mit dem Codieren:

[<img class=" wp-image-237 " title="HTML-Markup_Css-float" alt="Tutorial_Css_float_1" src="{{ site.url }}/assets/floating/Tutorial_Css_float_14.png" width="771" height="711"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_14.png)

&nbsp;

Dem Hauptcontainer übergeben wir ein ID-Attribut ‚#haupt‘, den DIV-Containern jeweils das Klassenattribut ‚.box‘. Damit ist das Grundgerüst auch schon fertiggestellt. Kommen wir zum CSS. Zuerst geben wir den Boxen ein einfaches Styling:

[<img class=" wp-image-215" title="Tutorial CSS float" alt="Tutorial_Css_float_2" src="{{ site.url }}/assets/floating/Tutorial_Css_float_2.png" width="774" height="86"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_2.png)

&nbsp;

Dem Hauptcontainer wird hier die Hintergrundfarbe Grau übergegeben, außerdem erhält er eine Breite von 500px.
  
Die DIV-Container mit dem Klassenattribut ‚box‘ bekommen ein etwas helleres Grau, zudem eine Höhe von 150px und eine Breite von 180px zugewiesen. Damit die Container visuell voneinander getrennt sind, weisen wir den DIV-Containern noch einen Rand von 10px zu. Wir erhalten schließlich folgendes Seitendesign:
[<img class="size-full wp-image-216" title="Tutorial float CSS" alt="Tutorial_Css_float_3" src="{{ site.url }}/assets/floating/Tutorial_Css_float_3.png" width="476" height="593"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_3.png)

&nbsp;

Da wir dem Hauptcontainer keine Höhe zugewiesen haben, passt er sich der Höhe den DIV-Containern an und erhält eine Höhe von 4x150px + ‚_margin_‘.
  
Da es sich beim DIV-Element um ein Block-Element handelt, werden die DIV-Container untereinander dargestellt, wie sie im HTML Dokument eingetragen sind. Jeder DIV-Container definiert einen neuen Absatz.

## DIV-Container mit float anordnen

Nun wollen wir aber mehr Kontrolle über die DIV-Container erlangen und sie z.B. innerhalb des Hauptcontainers nebeneinander anordnen. D.h. bei einer Breite des Hauptcontainers von 500px würden zwei DIV-Container jeweils nebeneinander passen. Wir wollen etwa folgendes Design erstellen:
[<img class="size-full wp-image-217" title="CSS Tutorial float" alt="Tutorial_Css_float_4" src="{{ site.url }}/assets/floating/Tutorial_Css_float_4.png" width="474" height="329"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_4.png)

&nbsp;

Nun kommen wir zum _float_ Befehl. Wenn wir diesen Befehl den DIV-Containern zuweisen, werden sie sich solange nebeneinander in einem Absatz positionieren,  wie der Absatz breit ist (in unserem Fall 500px). Wir fügen in unserem  CSS-Code also den _float_ Befehl den DIV-Containern zu und erhalten:

[<img class=" wp-image-218" title="CSS Tutorial float" alt="Tutorial_Css_float_5" src="{{ site.url }}/assets/floating/Tutorial_Css_float_5.png" width="795" height="29"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_5.png)
&nbsp;

Wenn wir uns jetzt das Design anschauen müssen wir jedoch feststellen, dass der Hauptcontainer wie vom Erdboden verschluckt ist:

[<img class="size-full wp-image-219" title="CSS Tutorial float" alt="Tutorial_Css_float_6" src="{{ site.url }}/assets/floating/Tutorial_Css_float_6.png" width="479" height="398"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_6.png)


Was ist passiert? Durch den _float_ Befehl wird der Hauptcontainer, in dem sich die ‚gefloateten‘ DIV-Container befinden, sozusagen ignoriert. Seine Höhe, die wir ja nicht festgelegt haben ist praktisch Null. Seine Breite ist hingegen noch definiert, da sich die Boxen weiterhin an der 500px Breite orientieren. Wie kann man den Hauptcontainer allerdings wieder sichtbar machen?

## Let’s clear the float

Dazu müssen wir zunächst zu unserem HTML-Code zurückkehren und folgenden DIV-Container hinzufügen:

[<img class=" wp-image-220" title="Tutorial CSS float" alt="Tutorial_Css_float_7" src="{{ site.url }}/assets/floating/Tutorial_Css_float_7.png" width="711" height="322" />]({{ site.url }}/assets/floating/Tutorial_Css_float_7.png)

Wir haben jetzt hinter die vier DIV-Container einen weiteren DIV-Container gestellt. Aber keine Angst, dieser wird später nicht im Seitendesign auftauchen. Er hilft uns lediglich dabei, unseren Hauptcontainer wieder sichtbar zu machen, der durch das _float_ scheinbar verschwunden ist.
  
Dem neuen DIV-Container haben wir ein ID-Attribut #clear hinzugefügt. Diese Bezeichnung ist allerdings frei gewählt und soll uns lediglich die Möglichkeit geben, den Container einzeln im CSS Dokument anzusprechen. Dieses Dokument erweitern wir nun um folgende Zeilen:
[<img class=" wp-image-221" title="CSS Tutorial float" alt="Tutorial_Css_float_8" src="{{ site.url }}/assets/floating/Tutorial_Css_float_8.png" width="730" height="45"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_8.png)

&nbsp;

Wir setzen alle Dimensionsmaße auf Null, da wir ja den DIV-Container scheinbar unsichtbar machen wollen. Entscheidend ist nun folgender Eintrag: _‚clear: both‘_. Hiermit wird der _float_-Befehl praktisch neutralisiert. Der Hauptcontainer wird wieder angezeigt, da seine Höhe nun wieder durch die DIV-Container definiert wird, ohne dass man jedoch den fünften DIV-Container sehen kann.

[<img class="size-full wp-image-222" title="Tutorial CSS float" alt="Tutorial_Css_float_9" src="{{ site.url }}/assets/floating/Tutorial_Css_float_9.png" width="499" height="336"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_9.png)
&nbsp;

Herzlichen Glückwunsch, nun haben wir mit _float_ einen Hauptcontainer erstellt, der nebeneinander angeordnete DIV-Container enthält.

## Float mit clearfix auflösen

Als Webworker wird einem allerdings von Anfang an eingebläut, dass man unnötiges Markup im HTML.-Dokument vermeiden sollte und Struktur und Layout stets trennen sollte. Diese „Good-Practices“ sind berechtigt, werden allerdings beide von der vorgenannten Lösung verletzt. Doch es gibt Abhilfe: Die _clearfix_ Lösung. Hierbei macht man es sich zunutze, das es in CSS die Möglichkeit gibt mit den ‚:_before_‘ und ‚:_after_‘ Werkzeugen, HTML-Elemente aus dem CSS Dokument heraus zu simulieren. Doch hierzu ein kleines Beispiel:
  
Nach dem Einfügen folgender Zeilen in das CSS-Dokument,
[<img class="size-full wp-image-223" title="Tutorial CSS float" alt="Tutorial_Css_float_10" src="{{ site.url }}/assets/floating/Tutorial_Css_float_10.png" width="514" height="487" />]({{ site.url }}/assets/floating/Tutorial_Css_float_10.png)
&nbsp;

Wie man sehen kann, wurde folgend, auf jeden DIV-Container, ein Inline-Element mit dem Text ‚Hallo Welt‘ eingefügt. Das können wir nun nutzen, um einen DIV-Container zu erstellen, wie wir ihn vorhin für das clear: both Werkzeug genutzt haben, um den _float_ Befehl zu neutralisieren. Dazu erstellen wir folgenden CSS-Code:

[<img class=" wp-image-224" title="CSS Tutorial float" alt="Tutorial_Css_float_11" src="{{ site.url }}/assets/floating/Tutorial_Css_float_11.png" width="738" height="278"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_11.png)
&nbsp;

Für den Selektor .clearfix haben wir folgende Regeln festgelegt: Erstelle nach dem Element mit dem Klassenattribut clearfix (dieser Name ist frei wählbar) Content mit dem Inhalt ‚.‘ (auch dieser Content ist frei wählbar), definiere dieses Element als Blockelement (wie ein DIV-Container) und verstecke seinen Inhalt (in diesem Fall den Punkt). Darüber hinaus nutzen wir das uns schon bekannte _clear: both_ Werkzeug, um das float der DIV-Container zu neutralisieren und dem Hauptcontainer eine Höhe zuzuweisen. Mithilfe eines height: 0; verhindern wir, dass der Hauptcontainer sich vergrößert. Jetzt müssen wir unserem Hauptcontainer noch diese Klasse zuweisen:
[<img class=" wp-image-238" title="CSS Tutorial float" alt="Tutorial_Css_float_12" src="{{ site.url }}/assets/floating/Tutorial_Css_float_121.png" width="633" height="342"  />]({{ site.url }}/assets/floating/Tutorial_Css_float_121.png)
&nbsp;

Schauen wir nun auf unser Seitendesign erhalten wir exakt das gleiche Ergebnis, wie zuvor mit dem DIV-Container .clear.

[<img class="size-full wp-image-226" title="CSS Tutorial float" alt="Tutorial_Css_float_13" src="{{ site.url }}/assets/floating/Tutorial_Css_float_13.png" width="490" height="325" />]({{ site.url }}/assets/floating/Tutorial_Css_float_13.png)

&nbsp;

Und dieses Ergebnis gelingt uns ganz ohne zusätzliches Markup in unserem HTML-Dokument.

Das war es auch schon. Ich hoffe das float und clear kein Buch mit sieben Siegeln mehr für euch darstellt und ihr in Zukunft eure HTML-Elemente besser im Griff habt, wenn es um das Thema Positionierung geht. Ich empfehle euch noch sehr ein Videotutorial (in emglish) der <a title="phpacademy - CSS float Video Tutorial " href="http://http://www.youtube.com/watch?v=rI-pc-MHNyk." target="_blank">phpacademy</a>, das diesen Themenbereich noch einmal intensiver beleuchtet. Für weitere Details empfehle ich zudem die offizielle <a title="W3C CSS" href="http://www.ich-lerne-css.de/" target="_blank">CSS-Einführung</a> des W3C.

Für professionelles Webdesign und innovative Designlösungen besucht auch meine Webseite:

<a title="webstudio Richter" href="http://www.webstudio-richter.de" target="_blank">http://www.webstudio-richter.de</a> (deutsch)

<a title="webstudio Richter" href="http://www.berlins-webdesigner.de " target="_blank">http://www.berlins-webdesigner.de </a>(english)
  
Viel Spaß bem Codieren!
