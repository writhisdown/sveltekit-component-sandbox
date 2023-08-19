<script>
	export let variant = null;
	export let modifier = null;
	export let title = null;
	export let ariaLabel = null;
</script>

<button
	on:click
	class:secondary={variant === 'secondary'}
	class:icon-only={modifier === 'icon-only'}
	type="button"
	{title}
	aria-label={ariaLabel}
>
	<slot />
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
		font-weight: 700;
		border: 1px solid #0369a1;
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

		& :global(svg) {
			fill: currentColor;
			width: 1rem;
			height: 1rem;
			pointer-events: none;
		}
	}

	.secondary {
		background: transparent;
		border-color: #94a3b8;
		color: #1e293b;

		&:hover {
			background: #e2e8f0;
		}

		&:active {
			background: #334155;
			color: #fff;
		}
	}

	.icon-only {
		padding: 8px;
	}
</style>
