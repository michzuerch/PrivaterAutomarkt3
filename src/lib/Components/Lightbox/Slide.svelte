<script>
	export let slideNo;
	export let totalSlides;
	export let image;
	export let altTag;
	export let attr;
</script>

<!-- Full-width images with number text -->
<div class="slides">
	<div class="text-white font-sm text-shadow-xl px-1 py-2 absolute top-0">
		{slideNo} / {totalSlides}
	</div>
	<img class="w-full" src={image} alt={altTag} title={attr} />
</div>
