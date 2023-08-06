<script>
	export let title;
	export let text;
	export let active;
</script>

<article class="tab-item" class:active>
	<h1>{title}</h1>
	<p>{text}</p>
</article>

<style>
	.tab-item {
		display: none;
	}

	p {
		font-size: 1rem;
		line-height: 1.5rem;
	}

	.active {
		display: block;
	}
</style>
