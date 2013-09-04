---
layout: post
title: "Adding Font Awesome to Octopress"
date: 2013-09-04 08:32
comments: true
categories: 
---

[This gist][2] together with [this post][3] and [this post][4] explaining how to add Font Awesome to Octopress simply don't work :[ 

Here are precise steps you have to take to make Font Awesome work.

<i class="icon-flag icon-2"></i>

* Download [Font Awesome][1].
 
* Extract contents :p

* Copy `font-awesome/scss` contents to  `OctoBlog/sass/font-awesome`
  so it becomes `OctoBlog/sass/font-awesome/scss`.

* Open `OctoBlog/sass/screen.scss` and add the line:
  `@import "font-awesome/scss/font-awesome.scss";`.

* Copy `font-awesome/font` folder to `OctoBlog/source` 
  so it becomes `OctoBlog/source/font`.

* Save files that you have modified.

* Now you can use Font Awesome! Simply add any icon like so:
  `<i class="icon-flag"></i> icon-flag` 

* `Ctrl`+`F5` to refresh the page and cache.

P.S.

You can also use `font-awesome/css` instead of scss as an alternative. Good luck!


 [1]: http://fortawesome.github.com/Font-Awesome/ "Font Awesome"
 [2]: https://gist.github.com/danielres/3157685
 [3]: http://avivkiss.com/blog/2013/03/03/using-font-awesome-with-octopress-how-to/
 [4]: http://nesterchung.github.io/blog/2013/05/23/use-font-awesome-on-octopress/