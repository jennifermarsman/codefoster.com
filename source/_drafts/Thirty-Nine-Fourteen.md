---
title: Thirty Nine Fourteen
tags: []
date: 
---

That's how many lines of CSS code make up the ui-light.css file that you get with WinJS.

What exactly are these nearly 4,000 lines of code doing for you? A lot of good stuff actually. And not only that, but there&rsquo;s a lot that can be learned from spending some time looking at this file with a microscope. The techniques used in it are pretty advanced as far as CSS goes, and there are some classes, pseudo-classes, and pseudo-elements that you&rsquo;ve likely not been introduced to yet.

All-in-all, the style sheet defines the look and feel of a Windows 8 app, all of its typography, all of the standard HTML controls, and all of the controls provided for you by WinJS such as ListView, slider, and many more.

[![](http://codefoster.blob.core.windows.net/site/image/3a15b2449c3643cd9642be5bc0d7f54a/3914_01_1.png "image")](http://{fix}/image.axd?picture=image_2.png)

Here are a few of the highlights I want to call out...

*   **header styles. **The font size and weight of the standard headers h1 through h6 are defined using the Windows 8 type ramp &ndash; 42pt, 20pt, 11pt, and 9pt. Also, along with each header is an accompanying class so that the font ramp can be applied to text elements without making them headers. For h1 there is win-type-xx-large, for h2 win-type-x-large, for h3 win-type-large, for h4 win-type-medium, for h5 win-type-small, and for h6 there's win-type-xx-small.
*   **win-type-ellipsis** is defined with the text-overflow: ellipsis property (and a couple of others) to allow text continuation
*   **HTML controls** such as button, progress, input, select, and textarea are defaulted with minimum widths and heights so they work well in a touch environment.
*   **win-backbutton** is defined as a class you can add to a button element to make it render like the round back button you see all over the place in Windows 8\. The various states of the button such as hover or disabled are defined as well.
*   **snapped media query. **When the user snaps an app, there's a lot less space for everything, so the size of the entire type ramp is reduced as is the size of the win-backbutton, the size of the appbar and appbar buttons, and the padding and margins in various places.
*   **high contrast **mode is supported throughout Windows 8 to improve visibility for people that need it. There is a media query expression for &ndash;ms-high-contrast that is captured in various media queries and defined to create more vivid contrasts and easier reading.

I&rsquo;m impressed with the CSS file and all of the time and consideration it must have taken to not only get all of these definitions written, but also to get them in the right order and to take into account things like the CSS specificity. There&rsquo;s very little in the file that feels remotely &ldquo;hacky&rdquo;. Still, I&rsquo;m glad I wasn&rsquo;t tasked with authoring it!