<script>
	import 'bootstrap/dist/css/bootstrap.min.css';
	// Navigation data
	let navigation = [
		{ text: 'Home', link: '#' },
		{ text: 'Products', link: '#products' },
		{ text: 'Pricing', link: '#pricing' },
		{ text: 'Contact', link: '#contact' }
	];
</script>

<main>
	<nav class="navbar navbar-expand-lg navbar-light bg-light">
		<div class="container">
			<a class="navbar-brand" href="#">Eye Products Store</a>
			<div class="collapse navbar-collapse" id="navbarNav">
				<ul class="navbar-nav ml-auto">
					{#each navigation as item ((item.text, item.link))}
						<li><a class="nav-link" href={item.link}>{item.text}</a></li>
					{/each}
				</ul>
			</div>
		</div>
	</nav>
</main>

<slot />
