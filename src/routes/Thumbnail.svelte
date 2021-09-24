<script>
	export let thumbimg;
	export let alttag;
	export let isActive;
</script>

<style>



/* Six columns side by side */
.tncolumn {
  float: left;
  width: 16.66%;
}

/* Add a transparency effect for thumnbail images */
.sample {
  opacity: 0.6;
}

.active,
.sample:hover {
  opacity: 1;
}
</style>

  
<div class="tncolumn">
	<img class="sample cursor" class:active={isActive} src={thumbimg} style="width:100%" on:click alt={alttag}>
</div>
