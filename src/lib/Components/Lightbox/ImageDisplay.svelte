<script>
	import { fade, fly } from 'svelte/transition';
	import { images } from './imageData.js';
</script>

<!-- Image Row -->
<div class="flex flex-wrap justify-center m-8">
	{#each images as { id, imgurl, name }}
		<div class="flex justify-center items-center w-1/4">
			<img
				class="w-1/2 border-solid border-black cursor-pointer m-1"
				{id}
				src={imgurl}
				alt={name}
				on:click
			/>
		</div>
	{/each}
</div>
