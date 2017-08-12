---
title: Web
---

*&larr; back to [Targets](%base_url%/?targets)*

# Web

## Font-Awesome

Amazing set of scalable icons.

One of the most useful things is being able to stack icons (cf. [examples page](http://fontawesome.io/examples/)):

```html
<span class="fa-stack fa-lg">
  <i class="fa fa-circle fa-stack-2x"></i>
  <i class="fa fa-flag fa-stack-1x fa-inverse"></i>
</span>
```

## Bootstrap

### Overview

Handy little library, great for:

- Responsive grid
- Navbar - see [navbar doco](https://getbootstrap.com/components/#navbar) (and [navbar example](https://getbootstrap.com/examples/navbar/))

### Themes

A lot of themes are paid, but [Bootswatch](https://bootswatch.com/) has open source themes! Yay!

## Responsive video container

```css
/*
 * Credits:
 *   https://coolestguidesontheplanet.com/videodrome/youtube/
 *
 */

.video-container {
	position:relative;
	padding-bottom:56.25%;
	padding-top:30px;
	height:0;
	overflow:hidden;
}

.video-container iframe, .video-container object, .video-container embed {
	position:absolute;
	top:0;
	left:0;
	width:100%;
	height:100%;
}
```
