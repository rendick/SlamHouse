<script>
	// @ts-nocheck

	import '../style.css';

	import { page } from '$app/stores';

	import Navbar from '../Navbar.svelte';
</script>

<svelte:head>
	<title>404 Not Found</title>
</svelte:head>

<Navbar />

<div class="container">
	<h1>Oops! Something went wrong.</h1>
	<h2>{$page.error.message}</h2>
	<a href="/">Go back to the homepage</a>
</div>

<style>
	h1,
	h2 {
		font-family: 'Navbar Font', sans-serif;
		color: #fdff00;
		transition: 0.1s;
	}

	a {
		font-family: 'Navbar Font', sans-serif;
		color: #fdff00;
		font-size: 20px;
		transition: 0.1s;
	}

	.container:hover a {
		color: #ffff00c9;
	}
</style>
