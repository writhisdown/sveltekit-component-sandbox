<script>
	import Button from '../../lib/Button.svelte';
	import IconChevronDown from '../../lib/Icon_ChevronDown.svelte';
	import IconClipboardChecked from '../../lib/Icon_Clipboard_Checked.svelte';
</script>

<section>
	<div>
		<Button label="click me" />
		<Button label="click me">
			<svelte:fragment slot="icon_prefix">
				<IconClipboardChecked />
			</svelte:fragment>
		</Button>
		<Button label="click me">
			<svelte:fragment slot="icon_suffix">
				<IconChevronDown />
			</svelte:fragment>
		</Button>
		<Button label="click me">
			<svelte:fragment slot="icon_prefix">
				<IconClipboardChecked />
			</svelte:fragment>
			<svelte:fragment slot="icon_suffix">
				<IconChevronDown />
			</svelte:fragment>
		</Button>
	</div>
</section>

<style>
	section {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		min-height: calc(100vh - 35.5px);
	}

	div {
		display: flex;
		gap: 1rem;
		flex-wrap: wrap;
	}
</style>
