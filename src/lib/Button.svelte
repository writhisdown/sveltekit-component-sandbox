<script>
	export let label;
</script>

<button on:click type="button">
	<slot name="icon_prefix" />
	{label}
	<slot name="icon_suffix" />
</button>

<style lang="scss">
	button {
		display: inline-flex;
		align-items: center;
		gap: 0.5rem;
		padding: 0.5rem 1rem;
		background: #0369a1;
		color: #fff;
		font-size: 1rem;
		font-weight: 500;
		border: 1px solid;
		border-radius: 0.5rem;
		white-space: nowrap;
		cursor: pointer;
		transition-property: background-color;
		transition-timing-function: cubic-bezier(0.4, 0, 0.2, 1);
		transition-duration: 150ms;

		&:hover {
			background: #0284c7;
		}

		&:active {
			background: #0c4a6e;
		}

		&:focus-visible {
			outline: 2px solid #4338ca;
			outline-offset: 2px;
		}

		& svg {
			fill: currentColor;
			width: 1rem;
			height: 1rem;
		}
	}
</style>
