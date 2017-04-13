---
id: 48
title: 'LESS CSS &#8211; einfach effizienteres Stylen!'
date: 2013-04-23T13:29:09+00:00
author: Phillip Richter
layout: post
guid: http://bestinnovations.de//?p=48
permalink: /effizienter-stylen-mit-lesscss/
categories:
  - CSS
---
<img class="alignleft" alt="http://verekia.com/wp-content/uploads/2011/10/less-css-logo.png" src="http://verekia.com/wp-content/uploads/2011/10/less-css-logo.png" width="199" height="81" />

Mit CSS bekommt man als Webdesigner ein mächtiges Werkzeug an die Hand, dass es ermöglicht, Inhalte einer Webseite sowohl ästhetisch als auch benutzerfreundlich zu gestalten. Die Grundstruktur eines CSS Stylesheets ist simpel. Mithilfe von Selektoren können Elemente im HTML Dokument direkt angesprochen werden. Dabei entstehen hintereinander angeordnete Style-Vorschriften, die, gerade bei komplexeren Websites, oft sehr schnell unübersichtlich werden können. Gerade in Zeiten des responsiven Webdesigns, das oft mit mehreren CSS Stylesheets einhergeht, ist LESS CSS ein willkommener Workflow-Optimierer.<!--more-->

Schon die Modifizierung einer Schriftart oder einer Farbe, die mehrfach im CSS-Dokument angegeben ist, endet oft in einer zeitaufwändigen Sucherei. Zudem schleichen sich immer wieder Fehler ein, da man vielleicht an einer versteckten Stelle vergessen hat, den Wert zu modifizieren. Selbst durch die &#8218;Ersetzen-Funktion&#8216; vieler Editoren ist man vor solchen Fehlern nicht gefeit, man denke hier nur an die Such-Optionen „vorwärts“ oder „rückwärts“ und die damit zusammenhängende Gefahr einige Stellen des Dokuments schlicht übersehen zu haben.

## Weniger CSS mit LESS CSS

Hier bietet LESS CSS eine willkommene Abhilfe. Der Lernaufwand ist gering und die übersichtliche Homepage von [LESS CSS](www.lesscss.de) gibt in wenigen Schritten einen guten Einblick in die Materie und die Funktionalität der Stylesheet-Sprache.

Ein großer Vorteil beim Erlernen von LESS CSS ist die Tatsache, dass man CSS und LESS CSS im Zweifel auch mischen kann, so wird der eigene Workflow nicht unterbrochen, auch wenn einem eine sinnvolle Umsetzung in LESS CSS gerade am Anfang nicht in jedem Fall einfällt. Natürlich sollte eine solche Stylesheet-Datei nicht zur Regel werden, schon alleine aufgrund der schwereren Wartbarkeit solcher gemischter LESS CSS-Dateien. Aber insbesondere in der Anfangszeit kann man einfach nur einige ausgewählte Features der dynamischen Stylesheetsprache nutzen.

### Variablen für mehr Flexibilität

Das einfachste aber ungeheuer zweckmäßige Feature von LESS CSS ist die Möglichkeit, Variablen zu nutzen. Wie im Eingangstext erwähnt, bietet sich dieses Feature an, um Farben, Schriftarten oder ähnliches, die mehrfach im Dokument gesetzt werden, zu Beginn des Dokuments in einer Variablen zu speichern. Dies bietet einem die Möglichkeit, wichtige Werte im Stylesheet im Handumdrehen zu modifiziert. Praktisch könnte das z.B. so aussehen:

`<br />
@farbe: #FF0000;`

@schriftart: &#8218;Molengo‘;

&nbsp;

Nachdem man diese Werte zugewiesen hat, kann man im Rest des Stylesheets einfach den gewählten Variablennamen mit dem vorrangehenden Klammeraffen angeben.

`<br />
p {`

color: @farbe;

font-family: @schriftart;

}

Gesetzt den Fall, die Farbe Rot und das Schriftbild Molengo wird an verschiedenen Stellen des Dokuments definiert, reicht es nun, den Variablenwert am Anfang der LESS CSS-Datei zu verändern.

### Funktionalität mit Mixins

Das zweite Feature von LESS CSS sind die sogenannten Mixins. Mit deren Hilfe lassen sich Werte einer Klasse an eine andere Klasse übergeben. Damit können komplette Deklarationen widerverwendet werden. Dies bietet sich zum Beispiel bei der box-shadow Eigenschaft an.
  
`<br />
.box-schatten (@shadow: 5px 5px 5px #000000){`

-moz-box-shadow: @shadow;

-webkit-box-shadow: @shadow;

box-shadow: @shadow;
  
}

div {

.box-schatten;

}

&nbsp;

Wie deutlich wird, kann man sich so z.B. das ständige Wiederholen der browserspezifischen Präfixe sparen, indem man Sie, wie bei den einfachen Variablen, einmal am Anfang des Dokuments festlegt. Durch das Hinzufügen von Parametern kann man die Werte, ähnlich wie bei Funktionen, modifizieren. Im Falle unseres Beispiels könnte man die Farbe oder Stärke des Schattens für verschiedene Elemente verändern, dabei allerdings stets die Klasse .box-schatten verwenden.
  
`<br />
div {`

.box-schatten(10px 5px 10px #d3d3d3);

}

### Logische Strukturierung und weniger Schreibarbeit durch Verschachtelung

Das dritte Feature von LESS CSS ist die sogenannte Verschachtelung. Dadurch lassen sich ewig lange Selektoren verhindern, die maßgeblich zur Unübersichtlichkeit einer CSS-Datei beitragen und den Schreibaufwand deutlich erhöhen.
  
In Standard-CSS werden Kind-Elemente zusammen mit Ihren Eltern-Elementen angesprochen. Mit LESS CSS werden die Kind-Elemente hingegen in die Eltern-Elemente verschachtelt. Auch hierfür möchte ich zur Verdeutlichung ein Beispiel angeben. Nehmen wir an, wir haben ein Hauptmenu mit der ID #mainmenu, das typischerweise aus einer ungeordneten Liste besteht und deren Listenelemente Links darstellen, die wiederum einen Hovereffekt zugewiesen bekommen. Im klassischen CSS könnte di e Strukturierung folgendermaßen aussehen:
  
`<br />
#mainmenu{}`

#mainmenu ul{}

#mainmenu ul li{}

#mainmenu ul a{}

#mainmenu ul li:hover{}

Mithilfe der Verschachtelung von LESS CSS können die einzelnen Selektoren nun aufeinander aufbauen. Dies sähe im Falle unseres Hauptmenüs folgendermaßen aus:
  
`<br />
#mainmenu {`

ul {

li{

a{

}

&:hover {

}}}}

Anstatt nun nach jedem Selektor eine geschlossene geschweifte Klammer zu setzen und das nächste Kind-Element von neuem anzusprechen, werden die einzelnen Selektoren, die sich innerhalb des #mainmenu-Containers befinden, ineinander verschachtelt.

### Vielfältige Möglichkeiten der Implementierung

Es gibt drei Möglichkeiten LESS CSS in Ihre Webseite zu implementieren. Für den Fall, dass man kein weiteres Javascript auf seiner Seite laden möchte, bietet sich die direkte Konvertierung der LESS CSS Dateien auf Ihrem Rechner in CSS an. Mithilfe von Tools, wie WinLess, werden die Dateien direkt nach dem Speichern in Ihrem bevorzugten Editor in einfaches CSS übersetzt und dabei auch gleich komprimiert. Damit erspart man sich das Hochladen der LESS CSS-Datei auf den Server und muss keinerlei Veränderungen auf der Webseite vornehmen.

Neben der serverseitigen Einbindung von LESS CSS, auf die ich hier nicht weiter eingehen möchte, da sie für den Anfänger im Normalfall nicht die erste Wahl sein wird (siehe hierzu: www.lesscss.de), kann LESS CSS mithilfe von less.js direkt auf Ihrer Webseite eingebunden werden. Dafür wird nach dem Einbinden der LESS CSS-Datei einfach die less.js geladen, was folgendermaßen aussehen könnte:
  
`<br />
<link rel="stylesheet/less" type="text/css" href="styles.less">`

<script src=&#8220;less.js&#8220; type=&#8220;text/javascript&#8220;></script>

Somit findet eine Konvertierung on-the-fly statt, die allerdings das Hochladen der LESS CSS-Datei auf Ihren Server erfordert.

## Fazit und Tutorials

In diesem Beitrag habe ich nur einige wichtige Features von LESS CSS vorgestellt. Die Stylesheet-Sprache bietet noch weitaus mehr, jedoch hoffe ich, mit dieser kurzen Einführung einen Eindruck davon gegeben zu haben, wie viel effizienter LESS CSS die Arbeit eines Webdesigners machen kann. Der Lernaufwand ist gering, die Dokumentation auch für Neulinge geeignet und die Implementierung simpel. Jonathan Verrecchia hat ein tolles [Tutorial](http://verekia.com/less-css/dont-read-less-css-tutorial-highly-addictive) zu LESS CSS verfasst, das eine LESS CSS Datei &#8222;from the scratch&#8220; erstellt. Wer lieber per Video lernen möchte, dem sei das zweiteilige [Videotutorial](http://www.youtube.com/watch?v=1l3JgDGl_Z8) von Charles Wood ans Herz gelegt.

Viel Spaß beim Ausprobieren wünscht,

Phillip Richter