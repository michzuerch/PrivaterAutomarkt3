<script lang="ts">
	let images = [
		{ title: '1', src: 'Autos/Gallery/1.jpg' },
		{ title: '2', src: 'Autos/Gallery/2.jpg' },
		{ title: '3', src: 'Autos/Gallery/3.jpg' },
		{ title: '4', src: 'Autos/Gallery/4.jpg' },
		{ title: '5', src: 'Autos/Gallery/5.jpg' },
		{ title: '6', src: 'Autos/Gallery/6.jpg' },
		{ title: '7', src: 'Autos/Gallery/7.jpg' },
		{ title: '8', src: 'Autos/Gallery/8.jpg' },
		{ title: '9', src: 'Autos/Gallery/9.jpg' },
		{ title: '10', src: 'Autos/Gallery/10.jpg' },
		{ title: '11', src: 'Autos/Gallery/11.jpg' },
		{ title: '12', src: 'Autos/Gallery/12.jpg' },
		{ title: '13', src: 'Autos/Gallery/13.jpg' },
		{ title: '14', src: 'Autos/Gallery/14.jpg' },
		{ title: '15', src: 'Autos/Gallery/15.jpg' },
		{ title: '16', src: 'Autos/Gallery/16.jpg' },
		{ title: '17', src: 'Autos/Gallery/17.jpg' }
	];
</script>

<section aria-label="Fotogallery">
	<div class="carousel ">
		<button class="carousel-button previous">&#8592;</button>
		<button class="carousel-button next">&#8594;</button>
		<ul>
			<li class="slide data-active">
				<img src={images[0].src} alt="0" />
			</li>
			<li class="slide">
				<img src={images[1].src} alt="0" />
			</li>
			<li class="slide">
				<img src={images[2].src} alt="0" />
			</li>
		</ul>
	</div>
</section>

<!-- <div class="max-w-fit carousel">
	{#each images as { title, src }, index}
		<div id="slide{index}" class="relative w-full pt-3 carousel-item">
			<img {src} alt={title} class="mx-5 object-fill aspect-w-16 aspect-h-9" />
			<div class="absolute flex justify-between transform -translate-y-1/2 left-5 right-5 top-6">
				<a href="#slide{previous(index)}" class="btn btn-circle"
					>❮ {index} / Previous {previous(index)}</a
				>
				<a href="#slide{next(index)}" class="btn btn-circle">❯ Next {next(index)}</a>
			</div>
		</div>
	{/each}
</div>
 -->
<style>
	*,
	*::before,
	*::after {
		box-sizing: border-box;
	}

	body {
		margin: 0;
	}

	.carousel {
		width: 100vh;
		height: 100vh;
		position: relative;
	}

	.slide {
		position: absolute;
		inset: 0;
		opacity: 0;
	}

	.slide > img {
		display: block;
		width: 100%;
		height: 100%;
		object-fit: cover;
		object-position: center;
	}

	.slide[data-active] {
		opacity: 1;
	}

	.carousel-button {
		position: absolute;
		background: none;
		border: none;
		font-size: 4rem;
		top: 50%;
		z-index: 2;
		transform: translateY(-50%);
	}
</style>
