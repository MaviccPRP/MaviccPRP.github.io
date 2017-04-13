---
id: 303
title: 'E.pages: Mit CSS zum individuellen Webshop'
date: 2013-09-27T09:22:13+00:00
author: Phillip Richter
layout: post
guid: http://bestinnovations.de//?p=303
permalink: /epages-mit-css-zum-individuellen-webshop/
categories:
  - CSS
---
[<img class="size-full wp-image-327 alignleft" alt="epages-logo" src="{{ site.url }}/assets/e-pages/epages-logo.jpg" width="200" height="47" />]({{ site.url }}/assets/e-pages/epages-logo.jpg)

Nachdem ich an dieser Stelle vor einiger Zeit den Amazon Webstore vorgestellt habe und wie man ihn mit CSS und JavaScript an die eigenen Bedürfnisse anpassen kann, möchte ich heute ein ähnliches Kurz-Tutorial für den Strato Webshop bzw. Epages präsentieren. Der Strato Webshop basiert auf Epages, einem E-Commerce System aus Hamburg. Epages besitzt zurzeit einen Marktanteil von etwa 15 Prozent. Die einfache Bedienbarkeit des Webshops und die hohe Reichweite von Strato, der dieses System als Mietshop intensiv vermarktet, lassen vermuten, dass sich Epages auch in Zukunft einen relevanten Marktanteil sichern wird.

<!--more-->

Epages ist durch seine einfache Bedienbarkeit und Skalierbarkeit bekannt. Das BackOffice, ist auch für Einsteiger schnell zu begreifen. Wirklich interessant ist der Shop allerdings erst dadurch, dass er sich mit CSS und JavaScript an die individuellen Bedürfnisse anpassen lässt. So hat man neben den zahlreichen vorgegebenen Design-Templates im Grunde unbeschränkte Gestaltungsmöglichkeiten. In diesem Tutorial möchte ich Schritt für Schritt erläutern, wie und wo man seinen CSS/JavaScript Code eingeben kann.

Da dieses Kurz-Tutorial nicht das BackOffice von Epages an sich erklärt, nenne ich nachfolgend einige nützliche Anlaufstellen und Tutorials:

  * http://www.epages.com/de/support/tutorials/ (Tutorials der Firma)
  * https://www.youtube.com/watch?v=vNmSrQo0284&list=PLwlbxFLhx1njH-VTmjpXeoBqMnishWboh (Video-Tutorial: Installation bis Produktpflege)
  * http://helpcenter.epages.com/Doc/ver\_6\_12_3/epages/Manual/de/MBO.pdf (Das Handbuch für Epages)

Zudem steht einem unter der Internetadresse http://community.epages.com/de/ eine lebendige Community zur Verfügung, falls einmal noch offene Fragen bleiben.

## Wie finde ich die CSS-Selektoren heraus?

Bevor man eigene Styles festlegen kann, muss man zunächst herausfinden, mit welchen Selektoren bestimmte HTML-Elemente angesprochen werden. Dazu benötigen wir eines der zahlreichen Webdeveloper Werkzeuge, wie <a title="Firebug" href="https://addons.mozilla.org/de/firefox/addon/firebug/" target="_blank">Firebug</a> oder die <a title="Chrome DevTools" href="https://developers.google.com/chrome-developer-tools/?hl=de" target="_blank">Chrome DevTools</a>. Hiermit lässt sich durch einen Rechtsklick auf das betreffende Element leicht herausfinden, welcher Selektor relevant ist.

&nbsp;

[<img class="alignnone size-full wp-image-306" alt="Epages-Firebug" src="{{ site.url }}/assets/e-pages/Epages-Firebug.png" width="984" height="623" srcset="http://bestinnovations.de/wp-content/uploads/2013/09/Epages-Firebug.png 984w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages-Firebug-300x189.png 300w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/e-pages/Epages-Firebug.png)

Im obigen Beispiel erkennt man, dass der Selektor für die ungeordnete Liste der Hauptnavigation .horizontal .navigation ist. Diese steckt wiederum im DIV-Container mit der ID #main_navigation. Mit dieser Methode lassen sich beliebige Elemente auf einer Webseite identifizieren.

## Wo gebe ich den CSS Code in Epages ein?

Hat man einen Selektor ausgewählt, begibt man sich in das BackOffice von Epages. Nach dem Login klickt man zunächst auf &#8222;Einstellungen&#8220; -> &#8222;Allgemeine Einstellungen&#8220; -> &#8222;Erweiterte Einstellungen&#8220;. Hier sieht man ein Fenster, in das man Code eingeben kann, der schließlich im HEAD-Bereich der Webseite landen wird. Aller Code, ob CSS oder JavaScript, wirkt sich global auf alle Seiten des Epages Webshops aus. Wie wir für spezifische Seiten Code eingeben erläutere ich anschließend.

&nbsp;

[<img class="alignnone size-full wp-image-308" alt="Epages-Erweiterte-Einstellungen" src="{{ site.url }}/assets/e-pages/Epages-Erweiterte-Einstellungen.png" width="1044" height="587" srcset="http://bestinnovations.de/wp-content/uploads/2013/09/Epages-Erweiterte-Einstellungen.png 1044w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages-Erweiterte-Einstellungen-300x168.png 300w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages-Erweiterte-Einstellungen-1024x575.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/e-pages/Epages-Erweiterte-Einstellungen.png)

Um nun der Hauptnavigation einen grünen Hintergrund zu geben, geben wir folgenden CSS-Code in das Fenster ein:

[<img class="alignnone  wp-image-309" alt="Code_1" src="{{ site.url }}/assets/e-pages/Code_1.png" width="302" height="136" />]({{ site.url }}/assets/e-pages/Code_1.png)

Zu beachten ist lediglich, dass man den CSS Code, wie gewohnt, innerhalb eines &#8217;style-tags&#8216; einfügt. Äquivalent sieht es mit JavaScript bzw. jQuery Code aus. Dieser muss innerhalb eines &#8217;script-tags&#8216; stehen.

## CSS in Epages für spezifische Seiten

Da sich die Selektoren auf verschiedenen Unterseiten des Epages Webshops nur selten ändern, muss, z.B. für Kategorie-spezifische Styles, der CSS/JavaScript Code woanders als im HEAD-Bereich eingegeben werden. Dazu verlassen wir die &#8222;Erweiterten Einstellungen&#8220; und klicken im Hauptmenü auf &#8222;Inhalt/Kategorien&#8220; -> &#8222;Vorschauansicht&#8220;.

[<img class="alignnone size-full wp-image-310" alt="Epages-Vorschauansicht" src="{{ site.url }}/assets/e-pages/Epages_Vorschauansicht.png" width="1095" height="456" srcset="http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Vorschauansicht.png 1095w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Vorschauansicht-300x124.png 300w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Vorschauansicht-1024x426.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/e-pages/Epages_Vorschauansicht.png)

Auf der linken Seite sehen wir nun alle Unterseiten/Kategorien unseres Webshops. Hier bekommt man auch einen guten Eindruck von der Webshop-Struktur. Um nun zum Beispiel eine spezifische CSS-Regel für die Kategorie Beauty festzulegen, etwa einen anderen Hintergrund, klicken wir zuerst auf die Kategorie. Anschließend klicken wir auf &#8222;Inhalt/Kategorien&#8220; -> &#8222;Datenblattansicht&#8220; -> &#8222;Text&#8220;.

[<img class="alignnone size-full wp-image-312" alt="Epages_Beschreibung" src="{{ site.url }}/assets/e-pages/Epages_Beschreibung.png" width="1044" height="537" srcset="http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Beschreibung.png 1044w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Beschreibung-300x154.png 300w, http://bestinnovations.de/wp-content/uploads/2013/09/Epages_Beschreibung-1024x526.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/e-pages/Epages_Beschreibung.png)

Diese Fenster sind normalerweise zur Eingabe von weiterer Beschreibung für die Kategorien vorgesehen. Da der Editor, ähnlich wie in WordPress oder Joomla, jedoch eine html-Funktion zur Verfügung stellt, kann man dort auch CSS und JavaScript Code eingeben, der nur dann ausgewertet wird, wenn die spezifische Seite aufgerufen wurde. Wichtig ist, bevor man den Code eingibt, die html Funktion mithilfe des Buttons oben rechts zu aktivieren. Daraufhin deaktivieren sich alle anderen Funktionen des Editors. Nun kann man, wie gewohnt, seinen CSS Code eingeben.

[<img class="alignnone  wp-image-313" alt="Code_2" src="{{ site.url }}/assets/e-pages/Code_2.png" width="376" height="210" srcset="http://bestinnovations.de/wp-content/uploads/2013/09/Code_2.png 470w, http://bestinnovations.de/wp-content/uploads/2013/09/Code_2-300x167.png 300w" sizes="(max-width: 376px) 85vw, 376px" />]({{ site.url }}/assets/e-pages/Code_2.png)

Mit den obigen CSS-Regeln wird nun etwa der Hintergrund beim Aufruf der Kategorie Beauty rot angezeigt. Falls man diese Regeln auch für die Unterkategorien des Epages Webshops aktivieren will, muss man sie nach obigem Verfahren für alle Unterseiten einzeln eingeben.

Damit sind wir auch schon am Ende dieses kleinen Tutorials angelangt. Ich hoffe ich konnte einige nützliche Tipps geben und freue mich über eure Kommentare und Anmerkungen. Bitte besucht auch unsere <a title="Web.studio Richter" href="https://www.facebook.com/webstudio.richter" target="_blank">Facebook </a>und <a title="webstudio Richer" href="https://plus.google.com/b/105357986131693436330/105357986131693436330/posts" target="_blank">Google Plus Accounts</a>.

Euer web.studio Richter

&nbsp;
