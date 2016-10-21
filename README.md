Hello!
To open the webpage,please click on index.html.The page would open up in your browser.


Optimizations made :

To index.html
1.Minify and inline style.css
2.Added a media query for the render blocking print.css
3.Used a webfrontloader to load google fonts asynchonously
4.Made the render blocking analytics.js async
5.Lossless compression of images(profile pic and pizzeria.jpg)

To main.js
1.
a)Create a variable randomPizzas to avoid querying of document.querySelectorAll(".randomPizzaContainer") and use this variable in the for loop
b)In the base code,we had a property offset width followed by a change in the Style.This causes a FSL.So,in the modified code,we have the changePizzaSizes determine the widths and in the for loop,it sets the width for every element to the corresponding percentage determined  by the switch statement.As pointed out by Cameron, there is no query selecting inside the for loop and hence,no FSL.So,there is a significant reduction in time to resize pizzas.

2.
a)items.length is stored in a variable ilen.
b)The value of (document.body.scrollTop / 1250) is initalized to a variable outside the for loop.
c)The repeating values are stored in a separate array arr.
d)getElementsByClassName is used instead of querySelectorAll.
e)items.length is stored in a variable ilen so that there wont be any iterations on that.
e)All of these optimizations were based on inputs from Office hours and fellow Udacians on the Discussion forum

