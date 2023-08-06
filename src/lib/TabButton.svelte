<script>
	export let label;
	export let selected;
</script>

<button on:click class:selected type="button">
	{label}
</button>

<style lang="scss">
	button {
		border: none;
		background: transparent;
		display: flex;
		justify-content: space-between;
		align-items: center;
		padding-inline: 12px;
		border-bottom: 3px solid transparent;
		height: 30px;
		color: #a4a4a4;
		font-size: 1rem;
		cursor: pointer;

		&:hover,
		&.selected {
			border-bottom: 3px solid #0fbeff;
		}
	}

	.selected {
		font-weight: 700;
		color: #1e293b;
	}
</style>
