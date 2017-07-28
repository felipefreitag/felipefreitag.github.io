---
layout: post
title:  "Random quote machine"
date:   2017-07-28 08:17:00 +0000
categories: frontend freecodecamp
---

# Random Quote Machine

This Free Code Camp challenge has the following instructions:

---
Build a Random Quote Machine

Objective: Build a CodePen.io app that is functionally similar to this: https://codepen.io/FreeCodeCamp/full/ONjoLe/.

Fulfill the below user stories. Use whichever libraries or APIs you need. Give it your own personal style.

+ User Story: I can click a button to show me a new random quote.

+ User Story: I can press a button to tweet out a quote.

---

It was my first experience using Javascript. I didn't even know what Jquery was!

Getting the API to work on Codepen wasn't that easy, I had to learn about cross-domain reference that Jquery kept complaining about. In later projects I found a workaround, but in this one I ended up using an Ajax call.

The Twitter function came from their website, I copied it and fiddled with it a little bit.

I used Bootstrap 4 and really liked the Card class, it's present in many other projects after this one.

Today, I'd refactor it to remove the global variable and function. And also to truncate the quote when clicking the Twitter button - if the quote is longer than 140 characters the user will have to edit it by hand.


<p data-height="265" data-theme-id="0" data-slug-hash="mmzeoZ" data-default-tab="result" data-user="felipefreitag" data-embed-version="2" data-pen-title="Random Quote Machine - Free Code Camp" class="codepen">See the Pen <a href="https://codepen.io/felipefreitag/pen/mmzeoZ/">Random Quote Machine - Free Code Camp</a> by Felipe Freitag Vargas (<a href="https://codepen.io/felipefreitag">@felipefreitag</a>) on <a href="https://codepen.io">CodePen</a>. </p>
<script  src="https://production-assets.codepen.io/assets/embed/ei.js"> </script>
