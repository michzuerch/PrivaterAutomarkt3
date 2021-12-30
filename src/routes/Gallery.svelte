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
<section class="w-full text-center mx-4 my-4">
	<button
		class="bg-yellow-600 hover:bg-yellow-800 text-white px-3 py-3 rounded text-lg shadow cursor-pointer"
		on:click={() => (modalOpen = true)}
	>
		Autogallerie
	</button>
</section>
