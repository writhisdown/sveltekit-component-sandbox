<div class="tab-container">
	<nav>
		<slot name="nav" />
	</nav>
	<div>
		<slot name="items" />
	</div>
</div>

<style>
	nav {
		display: flex;
	}

	.tab-container {
		padding: 0.75rem;
		max-width: 600px;
		width: 100%;
		border: 1px solid #cbd5e1;
		border-radius: 0.25rem;
		background: #fff;
		filter: drop-shadow(0 4px 3px rgb(0 0 0 / 0.07)) drop-shadow(0 2px 2px rgb(0 0 0 / 0.06));
	}
</style>
