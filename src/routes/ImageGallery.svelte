<script>
	import Slide from './Slide.svelte';
	import { images } from './imgdata.js';
	import Thumbnail from './Thumbnail.svelte';
	
	let imgShowIndex = 0;
	$: console.log(imgShowIndex);
	
	const prevSlide = () =>{
		if (imgShowIndex >= 1){
			imgShowIndex -=1;
		}		
	}

	const nextSlide = () =>{
		if (imgShowIndex <= images.length -2){
			imgShowIndex +=1;
		}
	}

	const gotoSlide = (idnumber) =>{
		imgShowIndex = idnumber;
		console.log("clicked on ",imgShowIndex);
	}
</script>

<style>		

/* Position the image container (needed to position the left and right arrows) */
.container {
  position: relative;
}
/* Next & previous buttons */
.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  margin-top: -50px;
  color: white;
  font-weight: bold;
  font-size: 20px;
  border-radius: 0 3px 3px 0;
  user-select: none;
  -webkit-user-select: none;
}
	
	
/* Position the "next button" to the right */
.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

/* On hover, add a black background color with a little bit see-through */
.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.tnrow:after {
  content: "";
  display: table;
  clear: both;
}
	
</style>

<div class="container">
	{#each images as {id,name, imguri }}
	<Slide imguri={imguri} 
				 alttag={name} 
				 title={name} 
				 currSlide={id+1} 
				 totalSlides={images.length}
				 imgShowing={id===imgShowIndex}/>
	{/each}
</div>
  <!-- Next and previous buttons -->
  <a href="#arrowL" class="prev" on:click={prevSlide}>&#10094;</a>
  <a href="#arrowR" class="next" on:click={nextSlide}>&#10095;</a>

<div class="tnrow">
	{#each images as {id, name, imguri} }
		<Thumbnail thumbimg={imguri} alttag={name} isActive={id===imgShowIndex} on:click={ () => gotoSlide(id) }  />
	{/each}
	
</div>