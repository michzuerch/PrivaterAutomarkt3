<script>
	import { createEventDispatcher } from 'svelte';
	export let caption;

	const dispatch = createEventDispatcher();

	function onkeydown(e) {
		//console.log(e.keyCode);
		switch (e.keyCode) {
			case 39:
				dispatch('nextClick');
				break;
			case 37:
				dispatch('prevClick');
				break;
		}
	}
</script>

<div class="flex justify-between items-center text-center bg-black text-xl px-2 py-4 text-white">
	<!-- Previous Arrow -->
	<a
		href="#arrowL"
		class="arrow cursor-pointer w-auto text-white text-3xl font-bold"
		on:click={() => dispatch('prevClick')}>&#10094;</a
	>
	<!-- Caption -->
	<p id="caption">{caption}</p>
	<!-- Next Arrow -->
	<a
		href="#arrowR"
		class="arrow cursor-pointer w-auto text-white text-3xl font-bold"
		on:click={() => dispatch('nextClick')}>&#10095;</a
	>
</div>
<svelte:window on:keydown={onkeydown} />
