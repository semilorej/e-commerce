<script>
	let navigation = [
		{ text: 'Home', link: '#' },
		{ text: 'Products', link: '#products' },
		{ text: 'Pricing', link: '#pricing' },
		{ text: 'Contact', link: '#contact' }
	];

	let isNavOpen = false;

	function toggleNav() {
		isNavOpen = !isNavOpen;
	}
</script>

<main>
	<nav class="navbar navbar-expand-lg navbar-light bg-light">
		<div class="container">
			<a class="navbar-brand" href="/">Eye Products Store</a>
			<button
				class="navbar-toggler"
				type="button"
				on:click={toggleNav}
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon" />
			</button>

			<div class="navbar-collapse" style="display: {isNavOpen ? 'block' : 'none'};">
				<ul class="navbar-nav ml-auto">
					{#each navigation as { text, link }}
						<li><a class="nav-link" href={link}>{text}</a></li>
					{/each}
				</ul>
			</div>
		</div>
	</nav>
</main>

<slot />
