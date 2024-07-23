<script>
	import Navbar from '../../Navbar.svelte';
</script>

<svelte:head>
	<title>FAQ</title>
</svelte:head>

<Navbar />

<div class="container">
	<div class="faq">
		<ul>
			<li>Bands from which countries will not be listed here? - From Russia.</li>
			<li>
				Which country's bands will you pay more attention to? - From Ukraine, but I will also be
				posting bands from other countries. Do not worry.
			</li>
			<li>
				Will there be other genres of death metal except Slamming/Brutal Death Metal? - Yeah, there
				will be.
			</li>
		</ul>
	</div>
</div>

<style>
	.container {
		color: #fdff00;
		font-family: 'Navbar font', sans-serif;
	}

	ul,
	li {
		text-align: center;
		list-style-position: inside;
		list-style-type: decimal;
            font-size: 17px;
	}
</style>
