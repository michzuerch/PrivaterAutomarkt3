<script lang="ts">
	import logo from './Logo.svg';
	import wave from './Wave.svg';
</script>

<header class="text-gray-800 body-font bg-yellow-500">
	<div class="container mx-auto flex flex-wrap p-3 flex-row items-stretch">
		<a
			href="/"
			class="flex title-font font-medium items-center text-base text-gray-900 mb-4 md:mb-0"
		>
			<img class="w-8" src={logo} alt="Company logo" />

			<span class="mx-3 text-xl font-extrabold">Privater Automarkt</span>
			<span class="hidden md:block text-xl font-extrabold">Radolfzell</span>
		</a>
		<nav class="md:ml-auto flex flex-wrap items-center text-base justify-center mb-4 md:mb-0">
			<a href="Gallery" class="mr-5 hover:text-gray-900">Galerie</a>
			<a href="Location" class="mr-5 hover:text-gray-900">Standort</a>
			<a href="Impressum" class="mr-5 hover:text-gray-900">Impressum</a>
		</nav>
	</div>
</header>
<img src={wave} alt="Wave" />
