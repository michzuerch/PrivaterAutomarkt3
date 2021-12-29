<script>
	import Lightbox from '$lib/Components/Lightbox/Lightbox.svelte';
	import ImageDisplay from '$lib/Components/Lightbox/ImageDisplay.svelte';

	let modalOpen = false;
	// $: console.log(modalOpen);

	let imageShowingIndex = 0;

	const handleImgClick = (e) => {
		imageShowingIndex = Number(e.target.id);
		modalOpen = true;
	};
</script>

<!-- The Modal/Lightbox -->
{#if modalOpen}
	<Lightbox on:click={() => (modalOpen = false)} {imageShowingIndex} />
{:else}
	<ImageDisplay on:click={handleImgClick} />
{/if}

<!-- Button to open Lightbox -->
<section class="w-full text-center mt-4">
	<button on:click={() => (modalOpen = true)}> Autogallerie </button>
</section>

<style>
	button {
		background-color: #000;
		color: white;
		padding: 10px 20px;
		box-shadow: 0 2px 3px black;
		cursor: pointer;
	}

	button:active {
		background-color: #555;
		color: white;
		box-shadow: none;
	}
</style>
