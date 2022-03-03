<script>
	import '../app.css';
	import 'flowbite/dist/flowbite.css';
	import Navbar from '$lib/Header/Navbar.svelte';
	import Footer from '$lib/Footer/Footer.svelte';
</script>

<Navbar />
<main>
	<slot />
</main>
<Footer />
