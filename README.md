# dev-parallax


DevParallax is a jQuery plugin which can give the parallax effect to the content

![Parallax Content](/clue-parallax.gif)

## Usage

Create parallax.css file in your assets and call them with link and put this code inside parallax.css

```css
.has-bg {
  background-repeat: repeat-y;
  background-position: 50%;
  background-size: cover;
}

.bg-size-auto {
  background-size: auto;
}

.bg-fixed {
  background-attachment: fixed;
}
```

and then call this script

```javascript
if( $.fn.parallax ) {
	$( '[data-background]' ).each(function() {
	   $( this ).parallax( $.extend( true, {
		lazyLoad: true, 
		mode: 'parallax', // none
		activeClass: 'has-bg', 
		fixedBgClass: 'bg-fixed', 
		parallaxClass: 'bg-fixed', 
		speedFactor: 0.3
	   }, $( this ).data() ) );
	});
}

```
