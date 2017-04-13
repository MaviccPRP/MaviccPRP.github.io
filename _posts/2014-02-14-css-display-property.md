---
title: The CSS display property
date: 2014-02-14T17:59:22+00:00
author: Phillip Richter
layout: post
permalink: /css-display-property/
categories: CSS
redirect_from: "/wordpress/css-display-property/"
---
<iframe width="560" height="315" src="//www.youtube.com/embed/G8sLEp20Zf4" allowfullscreen="" frameborder="0"></iframe>
  
This is a tutorial about the display property of CSS. Every HTML element is a rectangular. But there are several differences in their behavior on the page. While we have got block elements like the <p> text block element, the <div> container, the <h1>-<h4> headings or the <ul> list element, HTML comes as well with inline elements like the <span> tag, the <em> or <b> text element or the <img> image element.

Inline elements are mostly used in the flow of text, while block elements are for structuring a site. Inline elements accept padding and margin, but just the vertical values. The horizontal values are ignored by the surrounding elements. In addition, inline elements do not accept height or width properties.

Block elements in contrast accept margins, paddings and height and width properties. By default they are defining a start and end of a new line, using the whole space of the screen. To get them in one line you need to float these elements. As an alternative CSS comes with the inline-block value, which is widely supported by modern browsers.

By converting inline or block elements into inline-block elements, these elements behave like inline elements, plus they accept width and height properties. In addition the vertical paddings and margins are respected by the other HTML elements.

Last but not least, CSS display comes with the &#8217;none&#8216; value. Declaring a HTML element display: none, the element vanishes from the screen and is totally ignored by the other elements. Though the element is still in the DOM. You should not overuse this value, as screen readers will ignore these elements, too.

This tutorial gives a fundamental introduction to the CSS display property, using <a href="http://jsbin.com" target="_blank">JSBin</a>. Several examples will show the main differences between the inline, inline-block and block value. hope you have fun and this tutorial helps you a bit. I am happy about any comments!

Your web.studio
