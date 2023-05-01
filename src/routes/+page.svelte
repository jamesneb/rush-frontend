<script  lang="ts">
	import { ResponsiveGrid, SidebarNav } from 'rush-component-lib';
	import { Color, AnimationSettings, GridPlacementSettings, ColorSettings } from 'rush-component-lib';
	import type { SidebarStyles } from 'rush-component-lib';
	import { LinkSettings } from 'rush-component-lib';
	import { ButtonSettings } from 'rush-component-lib';

	let isGrid = true;
	let a = new AnimationSettings(0.3);
	let g = new GridPlacementSettings(1, 5, 1, 1);
	let c = new ColorSettings(Color.Rush_Black, Color.Rush_White);
	let l = new LinkSettings(12, Color.Rush_Grey, 10, Color.Rush_Link);
	let b = new ButtonSettings(Color.Rush_Orange, 40, 20, 16);

	let s: SidebarStyles = {
		grid: isGrid,
		animationSettings: a,
		gridPlacementSettings: g,
		colorSettings: c,
		linkSettings: l,
		buttonSettings: b
	}
</script>
<style>
		:global(body) {
				margin: 0;
				padding: 0;
				font-family: sans-serif;
		}
</style>

<ResponsiveGrid numRows = {4} numCols = {3} >
	<div slot='component' style="display: contents">
		<SidebarNav settings = {s} grid>

	</SidebarNav></div>

</ResponsiveGrid>
