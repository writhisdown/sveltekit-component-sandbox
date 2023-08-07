<script>
	import Button from '../../lib/Button.svelte';
	import IconChevronDown from '../../lib/Icon_ChevronDown.svelte';
	import IconClipboardChecked from '../../lib/Icon_Clipboard_Checked.svelte';
</script>

<section>
	<h1>Buttons Sandbox</h1>
	<div>
		<Button>click me</Button>
		<Button>
			<IconClipboardChecked />
			click me
		</Button>
		<Button>
			click me
			<IconChevronDown />
		</Button>
		<Button>
			<IconClipboardChecked />
			click me
			<IconChevronDown />
		</Button>
	</div>

	<div>
		<Button variant="secondary">click me</Button>
		<Button variant="secondary">
			<IconClipboardChecked />
			click me
		</Button>
		<Button variant="secondary">
			click me
			<IconChevronDown />
		</Button>
		<Button variant="secondary">
			<IconClipboardChecked />
			click me
			<IconChevronDown />
		</Button>
	</div>

	<div>
		<Button modifier="icon-only" title="icon button" ariaLabel="icon button">
			<IconClipboardChecked />
		</Button>
		<Button variant="secondary" modifier="icon-only" title="icon button" ariaLabel="icon button">
			<IconClipboardChecked />
		</Button>
	</div>
</section>

<style lang="scss">
	section {
		display: flex;
		flex-direction: column;
		width: 100%;
		min-height: calc(100vh - 35.5px);

		& h1 {
			margin: 1.5rem 0;
			font-size: 1.5rem;
			color: #1e293b;
		}
	}

	div {
		display: flex;
		gap: 1rem;
		flex-wrap: wrap;

		& + & {
			margin-top: 1rem;
		}
	}
</style>
