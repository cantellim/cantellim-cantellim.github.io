Part 1: Optimize PageSpeed Insights score for index.html

The Goal: a Google PageSpeed Insights score of 90 or higher for mobile and desktop.

The live page can be viewed at https://cantellim.github.io/. Copy the URL and paste it in the analyze field at PageSpeed Insights (https://developers.google.com/speed/pagespeed/insights/) to view the scores.

Optimizations:

I inlined the CSS stylesheet and the google font in the head of index.html. I also asynced loading of the javascript files by adding the async tag to them. I also resized the images, I tried to minimize the images using Gulp but was having trouble figuring out how to get that to work.

Part 2: Optimize Frames per Second in pizza.html

The Goal: Page renders at 60 frames per second when scrolling, the pizza size slider resizes pizza images in under 5ms.

The live page can be viewed at https://cantellim.github.io/. 

Optimizations:

Changes I made in views/js/main.js include replacing all querySelectorAlls with get ElementsByClassName for a more specific query. I changed the number of sliding pizzas to 24. I changed the function changePizzaSizes following the video from Browser Rendering Optimization course, under the Stop FSL section. Changed the function updatePostions first by taking the document.getElementsByClassName('mover'); outside of the function, than scrollPosition = document.body.scrollTop / 1250; out of the loop. I also changed the querySelector id with get ElementById in the changeSliderLabel function.
