<script>
	export let thumbImg;
	export let altTag;
	export let id;
	export let selected;
</script>

<div class="flex justify-center items-center w-2/12 bg-white">
	<img
		class="sample cursor-pointer w-full h-full opacity-80 hover:opacity-100"
		class:active={selected}
		{id}
		src={thumbImg}
		alt={altTag}
		on:click
	/>
</div>

<style>
	.active {
		opacity: 1;
	}
</style>
