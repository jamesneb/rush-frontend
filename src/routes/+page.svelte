<script  lang="ts">
	import { ResponsiveGrid, SidebarNav, HeaderNav, ContentArea } from 'rush-component-lib';
	import { Color } from 'rush-component-lib';
	import "$lib/fonts/printvetica.css";
	import { Motion, Unit } from 'rush-component-lib';
	import { PlacementMode } from 'rush-component-lib';


	let a = {scrollVelocity: 1, animationType: Motion.EASE_OUT}
	let g = {row: [1, 5], col:  [1, 1]}
	let c = {backgroundColor: Color.Rush_Orange, foregroundColor: Color.Rush_Grey};

	let sF = {ftMagnitude: 20, ftUnit: Unit.PX, ftFamily: "arial"}
	let sIF = {ftMagnitude: 15, ftUnit: Unit.PX, ftFamily: "arial"}
	let sIC = {backgroundColor: Color.Rush_Black, foregroundColor: Color.Rush_Teal, lnkColor: Color.Rush_Black, lnkHoverColor: Color.Rush_Teal};
	let sIB = {paddingMagnitude: 0, unit: Unit.PX};
	let sI = [{height: {magnitude: 20, unit: Unit.PX}, width: {magnitude: 20, unit: Unit.PX}, alt: 'profile', src: 'src/lib/icons/man.png',title: 'My Profile'},
						{height: 20, width: 20, alt: 'settings', src: '/icons/settings.png',title: 'Settings'},
						{height: 20, width: 20, alt: 'logout', src: '/icons/logout.png',title: 'Logout'}]

	let sBW = {magnitude: 50, unit: Unit.PX};
	let sBH = {magnitude: 50, unit: Unit.PX};
	let sBC = {backgroundColor: Color.Rush_Orange, foregroundColor: Color.Rush_Grey};

	let hI = [{title: 'Optimizer', path: '/optimizer'}, {title: 'Team', path: '/team'}, {title: 'Tasks', path: '/tasks'}];



</script>
<style>
		:global(body) {
				margin: 0;
				padding: 0;
				font-family: sans-serif;
		}
</style>

<ResponsiveGrid numRows = {4} numCols = {3} placementMode = {PlacementMode.EVENLY_SPACED} gridBgColor = {Color.Rush_Grey} >
	<div slot='component' style="display: contents">
		<SidebarNav gridPlacement = {g} animationSettings = {a} colorSettings = {c}
								sidebarFtSettings = {sF} sidebarItemFtSettings = {sIF}
								sidebarItemColorSettings = {sIC} sidebarItemBoxModelSettings = {sIB}
								sidebarItems = {sI} buttonWidth = {sBW} buttonHeight = {sBH}
								buttonColorSettings = {sBC} >

	</SidebarNav></div>
	<div slot='component2' style="display: contents">
		<HeaderNav items = {hI} >
		</HeaderNav>
	</div>
	<div slot='component3' style="display: contents">
		<ContentArea/></div>
</ResponsiveGrid>
