<script>
	import "../app.postcss";
    let open = false
</script>

<style global="" lang="postcss">
    @tailwind base;
    @tailwind components;
    @tailwind utilities;

	:global(body) {
		padding: 0;
	}
</style>


<slot></slot>