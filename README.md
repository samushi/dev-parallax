# dev-parallax


DevParallax is a jQuery plugin which can give the parallax effect to the content

![Parallax Content](/clue-parallax.gif)

## Usage


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
