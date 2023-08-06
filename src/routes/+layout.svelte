<script>
	import Header from '../lib/header.svelte';
</script>

<Header />

<main>
	<slot />
</main>

<style>
	@charset "UTF-8";

	:global(*) {
		-ms-box-sizing: border-box;
		box-sizing: border-box;
	}

	:global(body) {
		font-family: 'Inter', 'Arial', 'Verdana', sans-serif;
		color: #1e293b;
		margin: 0;
	}

	:global(a) {
		text-decoration: none;
	}

	main {
		width: 100%;
		min-height: calc(100vh - 35.5px);
		padding-inline: 1rem;
		margin-inline: auto;
	}
</style>
