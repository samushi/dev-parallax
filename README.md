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

html structure

```html
<!-- Parallax Background -->
<section class="padding paddv-120" data-background="demo/backgrounds/bg-02.jpg">
	<div class="container">
		<div class="row">
			<div class="col-md-12">
				<div class="parallax-content">
					<a class="icon" href="#" title="">
						<i class="pe-7s-arc"></i>
					</a>
					<h2>Steve Ballmer</h2>
					<p> The number one benefit of information technology is that it empowers people to do what they want to do. It lets people be creative. 
									<br>It lets people be productive. It lets people learn things they didn't think they could learn before, <br>and so in a sense it is all about potential.</p>	
					<a href="#" class="more white hvr-bounce-to-right">Learn More</a>	
				</div>
			</div>
		</div>
	</div>
</section>
<!-- END Parallax Background -->
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
