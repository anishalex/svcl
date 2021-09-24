<script>
	export let imguri;
	export let title;
	export let alttag;	
	export let totalSlides;
	export let currSlide;
	
	export let imgShowing;
</script>

<style>
/* Hide the images by default */
.mySlides {
  display: none;
}

/* Number text (1/3 etc) */
.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}
	img {
	width:100
	}
	.show {
  display: block;
}
</style>

<!-- Full-width images with number text -->
<div class="mySlides" class:show={imgShowing}>
	<div class="numbertext">{currSlide} / {totalSlides}</div>
	<img src={imguri} title={title} alt={alttag}>
</div>

