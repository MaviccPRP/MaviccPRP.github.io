---
id: 87
title: Mit CSS zum individuellen Amazon Webstore
date: 2013-05-23T08:37:23+00:00
author: Phillip Richter
layout: post
guid: http://bestinnovations.de//?p=87
permalink: /tutorial-schritt-fur-schritt-zum-individuellen-amazon-webstore-design/
categories:
  - CSS
redirect_from: "/wordpress/tutorial-schritt-fur-schritt-zum-individuellen-amazon-webstore-design/"
---
## [<img class=" wp-image-139 alignleft" alt="Amazon_Webstore_Logo" src="{{ site.url }}/assets/amazonwebstore/Amazon_Webstore_Logo.jpg" width="137" height="137" />]({{ site.url }}/assets/amazonwebstore/Amazon_Webstore_Logo.jpg)Der Amazon Webstore &#8211; einfach zum eigenen Webshop

<!--[if gte mso 9]><xml>

<o:OfficeDocumentSettings>

<o:AllowPNG/>

</o:OfficeDocumentSettings>

</xml><![endif]-->
<br>
Mit dem <a title="Amazon Webstore" href="http://webstore.amazon.de/" target="_blank">Amazon Webstore</a> bietet Amazon eine innovative E-Commerce-Lösung, die durch ihre einfache Bedienbarkeit und Wartung überzeugen kann. Jochen Weber vom t3n-Magazin hat hierzu einen <a title="Test Amazon Webstore" href="http://t3n.de/news/amazon-webstore-test-440924/" target="_blank">informativen Artikel</a> veröffentlicht, den ich wärmstens empfehlen kann. Insbesondere für kleine und mittelständige Unternehmen, die schon vorher über den Amazon Marketplace ihre Produkte vertrieben haben, ist der Lernaufwand für die Bedienung des Webstores minimal, da der Webstore ebenfalls wie der Marketplace über die Amazon Seller-Central bedient wird. Die Einpflegung von Produkten und die Erstellung von Kategorien, um nur einige Punkte zu nennen, verlaufen weitgehend nach dem gleichen Prinzip.<!--more-->

Im Gegensatz zum Marketplace, ermöglicht es der Amazon Webstore einem Unternehmen dem Onlineshop sein eigenes Branding und Design zu verpassen. Damit nutzt man weiterhin die zweifellos sehr gut ausgebaute Infrastruktur von Amazon, kann darüber hinaus aber auf sein eigenes Corporate Design zurückgreifen.

## Den Amazon Webstore Ihren Bedürfnissen anpassen

In diesem Tutorial möchte ich einige Tipps zu den Grundzügen der Designanpassung mit HTML/CSS erklären. Hierzu erläutere ich anhand zweier Beispiel wie die Arbeit mit CSS im Amazon Webstore in der Praxis aussieht. Es handelt sich nicht um eine Einführung in HTML/CSS, dazu verweise ich auf die sehr guten Tutorials von <a title="HTML5/CSS Tutorial" href="http://www.youtube.com/playlist?list=PL574801AD7ED44851" target="_blank">ScreendesignWhykiki</a> und vom <a title="CSS for Beginners" href="https://developer.mozilla.org/en-US/docs/Web/Guide/CSS/Getting_started?redirectlocale=en-US&redirectslug=CSS%2FGetting_Started" target="_blank">Mozilla Developer Network</a>. Da man im Amazon Webstore keinen direkten Zugriff auf die Layoutdateien via FTP hat, besteht die Möglichkeit die Dateien über ein Interface in der Seller Central zu erreichen. Dazu klickt man nach dem Einloggen auf den oberen Reiter ‚Shop-Design‘ woraufhin folgendes Pop-up Menü erscheint:

<img class="alignnone size-full wp-image-159" alt="Amazon Webstore Seller Central ShopDesign Merchandising und Layout" src="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-ShopDesign-Merchandising-und-Layout5.png" width="1024" height="396" srcset="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-ShopDesign-Merchandising-und-Layout5.png 1024w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-ShopDesign-Merchandising-und-Layout5-300x116.png 300w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />

Für unsere Arbeit am Amazon Webstore Design sind hier besonders die Punkte ‚_Merchandising und Layout_‘, ‚_Dateien verwalten_‘ und _‚Motive und Designs_‘ interessant. Durch die zahlreichen WYSIWYG-Tools von Amazon ist es möglich, sich ein Design ganz ohne Coding zusammenzustellen. Letztlich setzt dies aber voraus, dass entweder noch kein eigenes Firmendesign besteht, da die Anpassungsmöglichkeiten über die Tools nur begrenzt sind oder man allgemein kein großen Wert auf ein Shopdesign legt, schließlich wiederholen sich die „Layouts aus der Kiste“ nach einiger Zeit im Web.

Bevor wir eigene Layouts für den Amazon Webstore erstellen, müssen wir im Unterpunkt &#8218;_Motive und Designs_&#8218; zunächst ein Thema auswählen, das wir anschließend an unsere eigenen Bedürfnisse anpassen werden.

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motive.png"><img class=" wp-image-96 aligncenter" alt="Amazon Webstore Seller Central Motive" src="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motive.png" width="1456" height="786" srcset="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motive.png 1456w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Motive-300x161.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Motive-1024x552.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Auf dieser Seite können Sie nun vorkonfigurierte Themen von Amazon auswählen. Diese bestehen wiederum aus CSS-Dateien, Javascript und Bildern, die wir später modifizieren können. Auf der rechten Seite sind die verschiedenen Seiten des Amazon Webstore aufgelistet. Hier können Sie sich einen ersten Eindruck vom späteren Aussehen des Webstores machen. Über den Button oben rechts, ‚_Motiv anpassen_‘ können grundlegende Einstellungen vorgenommen werden, wie Schriftfarbe der Linktexte, Schriftart und Größe usw. Natürlich lässt sich das alles später auch manuell über die CSS-Dateien ändern.

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motiv-anpassen1.png"><img class=" wp-image-134 aligncenter" alt="Amazon Webstore Seller Central Motiv anpassen" src="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motiv-anpassen1.png" width="1456" height="786" srcset="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Motiv-anpassen1.png 1456w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Motiv-anpassen1-300x161.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Motiv-anpassen1-1024x552.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Nachdem man das Thema gewählt hat, kann man über den Unterpunkt &#8218;_Merchandising und Layout_&#8218; noch die Funktionalität der Website anpassen. Hier stehen verschiedene sogenannte Widgets zur Verfügung mit denen man z.B. Suchfelder, Produktlisten, Editorials u.a. einfügen kann. Durch klicken auf den Reiter &#8218;_Layout_&#8218; oben rechts lässt sich festlegen, wie viele Spalten, wie auf der Website angezeigt werden sollen.

Der zentrale Ort für das Codieren im Amazon Webstore ist der Unterpunkt ‚Dateien verwalten‘. Hier hat man Zugriff auf die zentralen Dateien des ausgewählten Grundmotivs. Nach dem Klicken auf diesen Unterpunkt erscheint folgendes Interface:

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Dateien-verwalten1.png"><img class=" wp-image-136 aligncenter" alt="Amazon Webstore Seller Central Dateien verwalten" src="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Dateien-verwalten1.png" width="1456" height="786" srcset="{{ site.url }}/assets/amazonwebstore/Amazon-Seller-Central-Dateien-verwalten1.png 1456w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Dateien-verwalten1-300x161.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/Amazon-Seller-Central-Dateien-verwalten1-1024x552.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Auf der linken Seite ist die Ordnerstruktur dargestellt, im rechten Feld erscheinen die jeweiligen Dateien. Der Ordner &#8218;_Merchandising Files_&#8218; ist für eigene Dateien bestimmt, die für das individuelle Website-Design verantwortlich sind. Im Ordner &#8218;_Theme Files_&#8218; befinden sich die Dateien des jeweils ausgewählten Themes.

Da man als Amazon Webstore Nutzer keinen direkten Zugriff auf die HTML-Dateien hat, es sei denn man integriert eigene HTML-Strukturen über die Widget-Oberfläche, nutzt man am besten den Firebug von Firefox oder die Dev Tools von Chrome, um an die Bezeichner der HTML-Elemente zu kommen. Zudem lassen sich die Bezeichnungen für die CSS-Selektoren über die Widget-Oberfläche herausfinden.

Jetzt jedoch genug der Theorie, lassen Sie uns anhand zweier Beispiele die Designanpassung in der Praxis testen.

## Beispiel 1: Anpassen der Navigationsleiste

Die Standard-Navigationsleiste des Basic-Themes ist nicht sonderlich ansehnlich, weshalb es sich lohnt, hier Hand anzulegen. Als Beispiel erstellen wir eine simple blaue Navigation, mit einzelnen Boxen pro Kategorie und abgerundeten Ecken. Unser Ergebnis soll folgendermaßen aussehen:

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/Navigation_blue.png"><img class=" wp-image-99 aligncenter" alt="Amazon Webstore Navigation_blue" src="{{ site.url }}/assets/amazonwebstore/Navigation_blue.png" width="921" height="57" srcset="{{ site.url }}/assets/amazonwebstore/Navigation_blue.png 921w, http://bestinnovations.de/wp-content/uploads/2013/05/Navigation_blue-300x18.png 300w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Zu Beginn müssen wir einige Änderungen an der &#8218;_widgets_master.css&#8216;_ des Basic-Themes vornehmen (Falls es hier eine bessere Möglichkeit gibt, bitte schreibt das in eure Kommentare). Mit dem Firebug-Tool kann man erkennen, dass ein Selektor für die Navigation ‚**_div.com-amazon-webstore-GlobalSiteNav-2 ul#globalNav_**‘ lautet. Diesen finden wir auch in der CSS-Datei.

<code style="font-weight: bold;">div.com-amazon-webstore-GlobalSiteNav-2 ul#globalNav {</code>
  
`background: url("http://ecx.images-amazon.com/images/I/01WeXtxfn5L.gif") repeat scroll 0 0 transparent;`
  
`border: 1px solid #CCCCCC;`
  
`height: auto;`
  
`list-style: none outside none;`
  
`margin: 0;`
  
`min-height: 40px;`
  
`padding: 0;`
  
`}`

Hier müssen wir nun die Zeilen für &#8218;_**background&#8216;**_ und &#8218;_**border&#8216;**_ auskommentieren, damit das schwarz/weiß gestreifte Hintergrundbild der Navigationsleiste und die Umrahmung verschwindet. Als nächsten Schritt kommentiert man die** _&#8218;background&#8216;_**-Angabe für den Hover-Zustand aus.

<code style="font-weight: bold;">div.com-amazon-webstore-GlobalSiteNav-2 ul#globalNav li.navigationGroup:hover, div.com-amazon-webstore-GlobalSiteNav-2 ul#globalNav li.navigationGroup.navigationHover {</code>
  
`background: url("http://ecx.images-amazon.com/images/I/211QXE2os9L.jpg") repeat-x scroll   left top transparent; z-index: 500;`
  
`}`

Nun haben wir eine einfache weiße Navigationsleiste, die nur darauf wartet, von uns ein wenig Farbe verpasst zu bekommen.

[<img class="alignnone  wp-image-100" alt="Amazon Webstore Navigation_white" src="{{ site.url }}/assets/amazonwebstore/Navigation_white.png" width="849" height="55" srcset="{{ site.url }}/assets/amazonwebstore/Navigation_white.png 849w, http://bestinnovations.de/wp-content/uploads/2013/05/Navigation_white-300x19.png 300w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/amazonwebstore/Navigation_white.png)

Die nächsten Schritte sind klassisches CSS-Coding. Am besten legt man sich zu Beginn eine eigene CSS-Datei an, wir nennen Sie in unserem Beispiel ‚_mycss.css_‘. Hier können wir der Navigationsleiste nun nach Herzenslust ein neues Design verpassen. Für unser blaues Menu könnte die CSS-Datei folgendermaßen aussehen:

`#header-9 div > ul > li { //Selektor für die Listeneinträge des Menüs`
  
`background-color: darkblue; //Setzt den Hintergrund der einzelnen Kategorie-Boxen auf Darkblue`
  
`border-radius: 5px 5px 5px 5px; //Runde Ecken`
  
`margin-right: 15px; //Hierdurch warden einzelne Boxen mit einem Abstand von 15px erstellt.`
  
`}`

<code style="font-weight: bold;">#header-9 span { //Setzt die Schriftfarbe auf weiß für bessere Lesbarkeit</code>
  
`color: white;`
  
`}`

Damit haben wir die Navigationsleiste auch schon angepasst. Ihr Amazon Webstore hat nun eine individuelle Navigationsleiste. Falls Dropdown-Menüs auf der Seite vorhanden sind, fährt man äquivalent fort. Zuerst werden eventuelle Ränder und Hintergrundbilder aus der &#8218;_widgets_master.css&#8216;_ auskommentiert, anschließend weißt man dem Menu ein eigenes Design über die &#8218;_mycss.css&#8216;_ zu.

## Beispiel 2: Einfügen eines eigenen HTML-Widgets

Als zweites Beispiel wollen wir ein eigenes HTML-Widget erstellen, den wir mit einfachem Text füllen und per CSS eine Umrandung mit abgerundeten Ecken zuweisen. Dies soll in etwa folgendermaßen aussehen:

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/Textbox.png"><img class=" wp-image-101 aligncenter" alt="Amazon Webstore Textbox" src="{{ site.url }}/assets/amazonwebstore/Textbox.png" width="1030" height="363" srcset="{{ site.url }}/assets/amazonwebstore/Textbox.png 1030w, http://bestinnovations.de/wp-content/uploads/2013/05/Textbox-300x105.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/Textbox-1024x360.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Zunächst begeben wir uns dazu in das Widget-Interface und wählen auf der linken Seite die Home-Seite aus. Nun ziehen wir mit gedrückter rechter Maustaste das HTML-Widget oben, auf einen beliebigen unteren Slot, z.B. E-1.

[<img class="alignnone  wp-image-98" alt="Amazon Webstore HTML-Widget_ziehen" src="{{ site.url }}/assets/amazonwebstore/HTML-Widget_ziehen.png" width="1456" height="786" srcset="{{ site.url }}/assets/amazonwebstore/HTML-Widget_ziehen.png 1456w, http://bestinnovations.de/wp-content/uploads/2013/05/HTML-Widget_ziehen-300x161.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/HTML-Widget_ziehen-1024x552.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" />]({{ site.url }}/assets/amazonwebstore/HTML-Widget_ziehen.png)

Im nächsten Schritt fügen wir einen beliebigen Inhalt in das HTML-Widget ein. In unserem Beispiel soll ein simpler Lorem Ipsum-Text ausreichen.<sup><br clear="all" /> </sup>

<p style="text-align: center;">
  <a href="{{ site.url }}/assets/amazonwebstore/HTML-Widget.png"><img class=" wp-image-97 aligncenter" alt="Amazon Webstore HTML-Widget" src="{{ site.url }}/assets/amazonwebstore/HTML-Widget.png" width="1456" height="786" srcset="{{ site.url }}/assets/amazonwebstore/HTML-Widget.png 1456w, http://bestinnovations.de/wp-content/uploads/2013/05/HTML-Widget-300x161.png 300w, http://bestinnovations.de/wp-content/uploads/2013/05/HTML-Widget-1024x552.png 1024w" sizes="(max-width: 709px) 85vw, (max-width: 909px) 67vw, (max-width: 1362px) 62vw, 840px" /></a>
</p>

Zum Stylen dieses HTML-Widgets setzt man seinen gewünschten HTML-Code einfach in ein DIV-Element und weißt diesem eine ID oder Klasse zu. In diesem Beispiel nennen verwenden wir die ID ‚_willkommen_‘. Die weiteren Schritte erklären sich von selber. Man bearbeitet nun die Datei ‚_mycss.css_‘ und fügt z.B. folgenden Code ein:

<code style="font-weight: bold;">#willkommen{</code>
  
`border: 1px solid black;`
  
`padding: 15px;`
  
`border-radius: 8px;`
  
`}`

Das war es auch schon! Solche HTML-Widgets kann man mit beliebigen Inhalten füllen, Javascript usw. Dadurch erhält man als Webdesigner freie Hand bei der Gestaltung des Webstores, falls es keine fertigen Widgets für die eigenen Anforderungen gibt.

Dieses kleine Tutorial soll nur einen kurzen Einblick in die Gestaltung des Amazon Webstores geben. Gerade bei solch proprietären Angeboten wie dem Amazon Webstore soll es Webdesignern, die keinen direkten Zugriff auf die Seller-Central haben einen Einblick in die Möglichkeiten der eigenen Gestaltung mittels CSS geben.

Letztlich hat man so auch die Möglichkeit einen responsiven Amazon Webstore zu entwickeln. Doch dazu werde ich in einem der nächsten Tutorials kommen. Sobald ich wieder etwas Zeit finde, werde ich zum Thema Amazon Webstore weitere Artikel veröffentlichen.

Vielen Dank und nicht vergessen dieses Tutorial zu ‚liken‘ und zu ‚sharen‘. Besuchen Sie auch meine Firmenwebsite: <a title="web.studio Richter" href="http://www.webstudio-richter.de" target="_blank">http://www.webstudio-richter.de</a>!

<!--[if gte mso 9]><xml>

<o:OfficeDocumentSettings>

<o:AllowPNG/>

</o:OfficeDocumentSettings>

</xml><![endif]-->

<!--[if gte mso 9]><xml>

<w:WordDocument>

<w:View>Normal</w:View>

<w:Zoom>0</w:Zoom>

<w:TrackMoves>false</w:TrackMoves>

<w:TrackFormatting/>

<w:HyphenationZone>21</w:HyphenationZone>

<w:PunctuationKerning/>

<w:ValidateAgainstSchemas/>

<w:SaveIfXMLInvalid>false</w:SaveIfXMLInvalid>

<w:IgnoreMixedContent>false</w:IgnoreMixedContent>

<w:AlwaysShowPlaceholderText>false</w:AlwaysShowPlaceholderText>

<w:DoNotPromoteQF/>

<w:LidThemeOther>DE</w:LidThemeOther>

<w:LidThemeAsian>X-NONE</w:LidThemeAsian>

<w:LidThemeComplexScript>X-NONE</w:LidThemeComplexScript>

<w:Compatibility>

<w:BreakWrappedTables/>

<w:SnapToGridInCell/>

<w:WrapTextWithPunct/>

<w:UseAsianBreakRules/>

<w:DontGrowAutofit/>

<w:SplitPgBreakAndParaMark/>

<w:EnableOpenTypeKerning/>

<w:DontFlipMirrorIndents/>

<w:OverrideTableStyleHps/>

</w:Compatibility>

<m:mathPr>

<m:mathFont m:val="Cambria Math"/>

<m:brkBin m:val="before"/>

<m:brkBinSub m:val="&#45;-"/>

<m:smallFrac m:val="off"/>

<m:dispDef/>

<m:lMargin m:val="0"/>

<m:rMargin m:val="0"/>

<m:defJc m:val="centerGroup"/>

<m:wrapIndent m:val="1440"/>

<m:intLim m:val="subSup"/>

<m:naryLim m:val="undOvr"/>

</m:mathPr></w:WordDocument>

</xml><![endif]-->

<!--[if gte mso 9]><xml>

<w:LatentStyles DefLockedState="false" DefUnhideWhenUsed="true"   DefSemiHidden="true" DefQFormat="false" DefPriority="99"   LatentStyleCount="267">

<w:LsdException Locked="false" Priority="0" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Normal"/>

<w:LsdException Locked="false" Priority="9" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="heading 1"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 2"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 3"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 4"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 5"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 6"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 7"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 8"/>

<w:LsdException Locked="false" Priority="9" QFormat="true" Name="heading 9"/>

<w:LsdException Locked="false" Priority="39" Name="toc 1"/>

<w:LsdException Locked="false" Priority="39" Name="toc 2"/>

<w:LsdException Locked="false" Priority="39" Name="toc 3"/>

<w:LsdException Locked="false" Priority="39" Name="toc 4"/>

<w:LsdException Locked="false" Priority="39" Name="toc 5"/>

<w:LsdException Locked="false" Priority="39" Name="toc 6"/>

<w:LsdException Locked="false" Priority="39" Name="toc 7"/>

<w:LsdException Locked="false" Priority="39" Name="toc 8"/>

<w:LsdException Locked="false" Priority="39" Name="toc 9"/>

<w:LsdException Locked="false" Priority="35" QFormat="true" Name="caption"/>

<w:LsdException Locked="false" Priority="10" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Title"/>

<w:LsdException Locked="false" Priority="1" Name="Default Paragraph Font"/>

<w:LsdException Locked="false" Priority="11" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Subtitle"/>

<w:LsdException Locked="false" Priority="22" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Strong"/>

<w:LsdException Locked="false" Priority="20" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Emphasis"/>

<w:LsdException Locked="false" Priority="59" SemiHidden="false"    UnhideWhenUsed="false" Name="Table Grid"/>

<w:LsdException Locked="false" UnhideWhenUsed="false" Name="Placeholder Text"/>

<w:LsdException Locked="false" Priority="1" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="No Spacing"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 1"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 1"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 1"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 1"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 1"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 1"/>

<w:LsdException Locked="false" UnhideWhenUsed="false" Name="Revision"/>

<w:LsdException Locked="false" Priority="34" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="List Paragraph"/>

<w:LsdException Locked="false" Priority="29" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Quote"/>

<w:LsdException Locked="false" Priority="30" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Intense Quote"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 1"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 1"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 1"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 1"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 1"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 1"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 1"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 1"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 2"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 2"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 2"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 2"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 2"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 2"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 2"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 2"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 2"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 2"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 2"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 2"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 2"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 2"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 3"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 3"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 3"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 3"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 3"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 3"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 3"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 3"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 3"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 3"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 3"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 3"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 3"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 3"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 4"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 4"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 4"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 4"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 4"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 4"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 4"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 4"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 4"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 4"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 4"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 4"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 4"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 4"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 5"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 5"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 5"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 5"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 5"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 5"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 5"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 5"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 5"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 5"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 5"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 5"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 5"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 5"/>

<w:LsdException Locked="false" Priority="60" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Shading Accent 6"/>

<w:LsdException Locked="false" Priority="61" SemiHidden="false"    UnhideWhenUsed="false" Name="Light List Accent 6"/>

<w:LsdException Locked="false" Priority="62" SemiHidden="false"    UnhideWhenUsed="false" Name="Light Grid Accent 6"/>

<w:LsdException Locked="false" Priority="63" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 1 Accent 6"/>

<w:LsdException Locked="false" Priority="64" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Shading 2 Accent 6"/>

<w:LsdException Locked="false" Priority="65" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 1 Accent 6"/>

<w:LsdException Locked="false" Priority="66" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium List 2 Accent 6"/>

<w:LsdException Locked="false" Priority="67" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 1 Accent 6"/>

<w:LsdException Locked="false" Priority="68" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 2 Accent 6"/>

<w:LsdException Locked="false" Priority="69" SemiHidden="false"    UnhideWhenUsed="false" Name="Medium Grid 3 Accent 6"/>

<w:LsdException Locked="false" Priority="70" SemiHidden="false"    UnhideWhenUsed="false" Name="Dark List Accent 6"/>

<w:LsdException Locked="false" Priority="71" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Shading Accent 6"/>

<w:LsdException Locked="false" Priority="72" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful List Accent 6"/>

<w:LsdException Locked="false" Priority="73" SemiHidden="false"    UnhideWhenUsed="false" Name="Colorful Grid Accent 6"/>

<w:LsdException Locked="false" Priority="19" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Subtle Emphasis"/>

<w:LsdException Locked="false" Priority="21" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Intense Emphasis"/>

<w:LsdException Locked="false" Priority="31" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Subtle Reference"/>

<w:LsdException Locked="false" Priority="32" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Intense Reference"/>

<w:LsdException Locked="false" Priority="33" SemiHidden="false"    UnhideWhenUsed="false" QFormat="true" Name="Book Title"/>

<w:LsdException Locked="false" Priority="37" Name="Bibliography"/>

<w:LsdException Locked="false" Priority="39" QFormat="true" Name="TOC Heading"/>

</w:LatentStyles>

</xml><![endif]-->

<!--[if gte mso 10]>





<![endif]-->
