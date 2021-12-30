<script>
	import { fade, fly } from 'svelte/transition';
	import { images } from './imageData.js';
	import Slide from './Slide.svelte';
	import Thumbnail from './Thumbnail.svelte';
	import Caption from './Caption.svelte';

	/* IMAGE TO SHOW */
	export let imageShowingIndex = 0;
	$: console.log(imageShowingIndex);
	$: image = images[imageShowingIndex];

	const nextSlide = () => {
		if (imageShowingIndex === images.length - 1) {
			imageShowingIndex = 0;
		} else {
			imageShowingIndex += 1;
		}
	};

	const prevSlide = () => {
		if (imageShowingIndex === 0) {
			imageShowingIndex = images.length - 1;
		} else {
			imageShowingIndex -= 1;
		}
	};

	const goToSlide = (slideID) => (imageShowingIndex = Number(slideID));
</script>

<section
	class="fixed z-10 left-0 top-0 w-full h-full overflow-auto bg-black flex justify-center items-center"
	in:fly={{ x: -300 }}
	out:fade
>
	<span
		class="text-white absolute top-2 right-2 font-extralight text-2xl hover:cursor-pointer hover:text-gray-400 hover:no-underline"
		on:click>&#10007;</span
	>

	<main class="w-10/12 flex flex-col bg-black">
		<!-- image gallery -->
		<div class="relative">
			<Slide
				image={image.imgurl}
				altTag={image.name}
				attr={image.attribution}
				slideNo={image.id + 1}
				totalSlides={images.length}
			/>
		</div>

		<!-- Image text -->
		<Caption
			caption={images[imageShowingIndex].name}
			on:prevClick={prevSlide}
			on:nextClick={nextSlide}
		/>

		<!-- Thumbnail images -->
		<div class="w-full flex self-end">
			{#each images as { id, imgurl, name }}
				<Thumbnail
					thumbImg={imgurl}
					altTag={name}
					{id}
					selected={Number(imageShowingIndex) === id}
					on:click={() => goToSlide(id)}
				/>
			{/each}
		</div>
	</main>
</section>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Josefin+Sans:wght@500&display=swap');

	* {
		box-sizing: border-box;
		font-family: 'Josefin Sans', sans-serif;
	}
</style>
