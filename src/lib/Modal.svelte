<script>
	import Button from './Button.svelte';
	import IconXmark from './Icon_Xmark.svelte';
	export let ariaLabeledBy;
	export let id;
	export let heading;
	export let rootElement;

	function closeModal() {
		rootElement.close();
		// console.log(rootElement);
	}
</script>

<dialog bind:this={rootElement} aria-labelledby={ariaLabeledBy} class="modal">
	<header class="modal__header">
		<h1 {id}>{heading}</h1>
		<Button on:click={closeModal} variant="secondary" modifier="icon-only" ariaLabel="close modal">
			<IconXmark />
		</Button>
	</header>
	<div class="modal__body">
		<slot name="modalBody" />
	</div>
	<div class="modal__actions">
		<slot name="modalActions" />
	</div>
</dialog>

<style lang="scss">
	.modal {
		display: flex;
		flex-direction: column;
		gap: 1.125rem 0;
		padding: 1.125rem;
		background: #fff;
		border: 2px solid #94a3b8;
		border-radius: 0.5rem;
		max-width: 768px;
		width: 100%;

		&:not([open]) {
			display: none;
		}

		&__header {
			display: flex;
			align-items: start;
			gap: 0 0.5rem;

			h1 {
				font-size: 1.5rem;
				color: #1e293b;
				width: 100%;
				margin: 0;
			}
		}

		&__body {
			font-size: 1rem;

			& :global(p) {
				margin: 0;
			}

			& :global(p + p) {
				margin-bottom: 1.125rem;
			}
		}

		&__actions {
			display: flex;
			align-items: center;
			justify-content: end;
			gap: 0 0.5rem;
		}
	}
</style>
