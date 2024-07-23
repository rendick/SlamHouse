<script>
	import Navbar from '../Navbar.svelte';
	import myjson from './music.json';

	let searchQuery = '';
	let genreQuery = '';
	let bandQuery = '';
	let countryQuery = '';

	$: filteredMusic = myjson.filter(
		(music) =>
			music.name.toLowerCase().includes(searchQuery.toLowerCase()) &&
			music.genre.toLowerCase().includes(genreQuery.toLowerCase()) &&
			music.band.toLowerCase().includes(bandQuery.toLowerCase()) &&
			music.country.toLowerCase().includes(countryQuery.toLowerCase())
	);
</script>

<svelte:head>
	<title>Slam House</title>
</svelte:head>

<Navbar />

<div class="container">
	<div class="search">
		<input
			type="text"
			bind:value={searchQuery}
			placeholder="Search by title..."
			class="search-input"
		/>
		<input
			type="text"
			bind:value={genreQuery}
			placeholder="Search by genre..."
			class="search-input"
		/>
		<input
			type="text"
			bind:value={bandQuery}
			placeholder="Search by band..."
			class="search-input"
		/>
		<input
			type="text"
			bind:value={countryQuery}
			placeholder="Search by country..."
			class="search-input"
		/>
	</div>

	{#each filteredMusic as music}
		<iframe
			title={music.name}
			country={music.country}
			style="border: 0; width: 150px; height: 300px"
			src={music.bandcamp_url}
			seamless
		>
		</iframe>
	{/each}
</div>

<style>
	iframe {
		padding: 5px;
	}
	.search-input {
		margin-bottom: 20px;
		padding: 10px;
		width: 100%;
		box-sizing: border-box;
	}

	::placeholder {
		color: #000000;
		opacity: 1;
	}
	.search {
		display: flex;
		gap: 10px;
	}

	input {
		background-color: #fdff00;
		font-family: 'Navbar font', sans-serif;
	}

	@media screen and (max-width: 500px) {
		.search {
			display: block;
		}
	}
</style>
