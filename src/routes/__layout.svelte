<script>
	import '../app.css';
	import Navbar from '$lib/Header/Navbar.svelte';
	import Footer from '$lib/Footer/Footer.svelte';
</script>
<svelte:head>
  <title>Privater Automarkt Radolfzell</title>:
</svelte:head>
<Navbar />
<main class="bg-wave">
	<slot />
</main>
<Footer />

<style>
	.bg-wave {
		background-image: url('wave.svg');
		background-repeat: no-repeat;
	}
</style>
