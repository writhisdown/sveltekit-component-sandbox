<script>
	import Button from '../../lib/Button.svelte';
	import Modal from '../../lib/Modal.svelte';

	let modal;

	function openModal() {
		modal.showModal();
		// console.log(modal);
	}
</script>

<h1>Modal Sandbox</h1>

<Button on:click={openModal}>Open modal</Button>

<Modal
	bind:rootElement={modal}
	ariaLabeledBy="Modal example"
	id="Modal example"
	heading="Modal header"
>
	<p slot="modalBody">
		Vegan tumeric palo santo single-origin coffee, hexagon pitchfork green juice. Hammock literally
		hoodie plaid, trust fund helvetica shaman blue bottle single-origin coffee la croix godard
		chillwave narwhal skateboard fashion.
	</p>
	<svelte:fragment slot="modalActions">
		<Button variant="secondary">Cancel</Button>
		<Button>Save</Button>
	</svelte:fragment>
</Modal>

<style lang="scss">
	h1 {
		margin: 1.5rem 0;
		font-size: 1.5rem;
		color: #1e293b;
	}
</style>
