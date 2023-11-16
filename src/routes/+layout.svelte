<script>
	let navigation = [
		{ text: 'Home', link: '#' },
		{ text: 'Products', link: '#products' },
		{ text: 'Pricing', link: '#pricing' },
		{ text: 'Contact', link: '#contact' }
	];

	let isNavbarOpen = false;

	function toggleNavbar() {
		isNavbarOpen = !isNavbarOpen;
	}
</script>

<main>
	<nav class="navbar navbar-expand-lg navbar-light bg-light">
		<div class="container">
			<a class="navbar-brand" href="/">Eye Products Store</a>
			<button
				class="navbar-toggler"
				on:click={toggleNavbar}
				aria-expanded={isNavbarOpen ? 'true' : 'false'}
				aria-label="Toggle navigation"
			>
				<span class="navbar-toggler-icon" />
			</button>
			{#if !isNavbarOpen}
				<div class="navbar-collapse" id="navbarNav">
					<ul class="navbar-nav ml-auto">
						{#each navigation as { text, link }}
							<li><a class="nav-link" href={link}>{text}</a></li>
						{/each}
					</ul>
				</div>
			{/if}
		</div>
	</nav>
</main>

<slot />
