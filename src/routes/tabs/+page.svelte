<script>
	import TabButton from '../../lib/TabButton.svelte';
	import TabItem from '../../lib/TabItem.svelte';
	import Tabs from '../../lib/Tabs.svelte';

	let currentTab = 0;

	let tabs = [
		{
			label: 'Tab 1',
			title: 'Item 1',
			text: "You probably haven't heard of them food truck brunch sriracha"
		},
		{
			label: 'Tab 2',
			title: 'Item 2',
			text: 'Bodega boys franzen pickled XOXO disrupt paleo direct trade brunch tousled selvage typewriter cronut.'
		},
		{
			label: 'Tab 3',
			title: 'Item 3',
			text: 'Hashtag meditation dreamcatcher, cold-pressed aesthetic ethical drinking grailed umami shabby chic poutine fit.'
		},
		{
			label: 'Tab 4',
			title: 'Item 4',
			text: 'Unicorn fashion axe celiac letterpress, neutral milk hotel meggings marxism praxis.'
		}
	];
</script>

<section>
	<Tabs>
		<svelte:fragment slot="nav">
			{#each tabs as tab, index}
				<TabButton
					on:click={() => (currentTab = index)}
					label={tab.label}
					selected={index === currentTab}
				/>
			{/each}
		</svelte:fragment>

		<svelte:fragment slot="items">
			{#each tabs as tab, index}
				<TabItem title={tab.title} text={tab.text} active={index === currentTab} />
			{/each}
		</svelte:fragment>
	</Tabs>
</section>

<style>
	section {
		display: flex;
		align-items: center;
		justify-content: center;
		width: 100%;
		min-height: calc(100vh - 35.5px);
	}
</style>
