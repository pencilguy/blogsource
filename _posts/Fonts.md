---
title: Fonts
date: 2016-04-14 23:19:07
tags: Web
---

### Where are the fonts ?
I didn't know how to add new fonts to web pages before. I thought the local fonts are available on webpages by default, and adding local fonts will do the magic. Well, that may really works, I don't know. But I find a far better way [here](http://baoxiehao.com/2015/02/01/Learn%20to%20Code%20HTML%20&%20CSS%2006/).
when we want to add our local fonts(downloaded from internet), we need to write css like this:
```css
@font-face {
  font-family: "Lobster";
  src: local("Lobster"), url("lobster.woff") format("woff");
}
```
Then you can use it like:
```css
body {
  font-family: "Lobster";
}
```
And if we want to use remote fonts, we can write like this:
```css
@font-face {
  font-family: 'Lobster';
  src: local('Lobster'), url(https://fonts.gstatic.com/s/lobster/v16/c28rH3kclCLEuIsGhOg7evY6323mHUZFJMgTvxaG2iE.woff2) format('woff2');
}
```
And today, I find the **awesome**, **cool**, **wonderful**, **amazing** precious: [**the google fonts**](https://www.google.com/fonts).
I am a little upset that I didn't heard it before, how could it be?

Anyway, font will not be a problem anymore !
