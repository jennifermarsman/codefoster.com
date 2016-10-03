---
title: Box Sizing
tags: []
date: 
---

Don't miss the box-sizing property in CSS. It's important. I'll tell you why.

Let me start by showing you a diagram of the HTML box model.

[![](http://codefoster.blob.core.windows.net/site/image/cdcacee2955f44b3b4f975001c44b377/boxsizing_01_1.png)](http://www.w3.org/wiki/images/d/d2/Boxarea.png)

Let's talk about a div, for example. If you create a div and then use CSS to assign some margin, a border, and some padding as well as the content that you include within the div element, you would end up with something that looks like the image above. Most people with some HTML and CSS experience are very familiar with this.

When you set the size (width or height) of that div using CSS, the size values that you specify apply in an... um... interesting way. The size values apply to the _content area_. That's a little bizarre, because in real life (the one we're all familiar with) when we talk about the size of a box of stuff, we are talking about the size of the _outside_ of the box.

This is a problem because if you want to set an element to the width of the screen and you use <span style="font-family: Consolas; background-color: rgb(217, 217, 217);">width:100%</span>, even that 100% does not include the padding, border, and margin, so if you have any of those then your box will run off the edge of the screen.

You can change this behavior though with a simple CSS property. If you set box-sizing to border-box (instead of the default content-box), then the same value of 100% for your div's width will now include the border and padding. It will still not include the margin, by the way.

Hope that helps.