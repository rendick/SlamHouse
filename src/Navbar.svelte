<script>
	import './style.css';
	let NavbarText = {
		HomePage: 'Home',
		FaqPage: 'FAQ',
	};
</script>

<div class="header">
	<div class="header-center">
		<a href="/">{NavbarText.HomePage}</a>
		<a href="/faq">{NavbarText.FaqPage}</a>
	</div>
</div>

<style>
	.header {
		overflow: hidden;
		background-color: #000000;
		display: flex;
		justify-content: space-between;
		align-items: center;
	}

	.header a {
		font-family: 'Navbar Font', sans-serif;
		color: #fdff00;
		text-align: center;
		padding: 12px;
		text-decoration: none;
		font-size: 30px;
		line-height: 25px;
		transition: 0.1s;
	}

	.header a:hover {
		color: #ffff00c9;
	}

	.header-center {
		display: flex;
		justify-content: center;
		flex: 1;
	}

	@media screen and (max-width: 500px) {
		.header {
			flex-direction: column;
		}
		.header a {
			float: none;
			display: block;
			text-align: left;
		}
		.header-center {
			float: none;
			justify-content: flex-start;
		}
	}
</style>
