<script>
	import { 
		Header,
		HeaderNav,
		HeaderNavItem,
		SideNav,
		SideNavItems,	
		SideNavLink
	} from "carbon-components-svelte";

	import Finance32 from "carbon-icons-svelte/lib/Finance32";
	import Idea32 from "carbon-icons-svelte/lib/Idea32";
	import Microscope32 from "carbon-icons-svelte/lib/Microscope32";

	let iAccounts = {
		class: undefined,
		skeleton: false,
		render: Finance32,
		title: "Accounts",
		tabindex: "0",
		focusable: false,
		style: undefined
	}

	let iIdeas = {
		class: undefined,
		skeleton: false,
		render: Idea32,
		title: "Ideas",
		tabindex: "0",
		focusable: false,
		style: undefined
	}

	let iResearch = {
		class: undefined,
		skeleton: false,
		render: Microscope32,
		title: "Research",
		tabindex: "0",
		focusable: false,
		style: undefined
	}

	/**
	 * @type {boolean} 
	 * 
	 */
	let isSideNavOpen = false;
	
	/**
	 * Holds the window width to handle resizing and menus 
	 * @type {integer} 
	 */
	let winWidth = undefined;
</script>
<svelte:head>
  <link
    rel="stylesheet"
    href="https://unpkg.com/carbon-components/css/carbon-components.min.css"
  />
</svelte:head>

<svelte:window bind:innerWidth={winWidth} />

<main>
	<Header bind:isSideNavOpen platformName="PMGR">
		<!-- Only display Header links if the window is large enough-->
		{#if winWidth >= 1056}
		<HeaderNav>
			<HeaderNavItem text="Accounts" />
			<HeaderNavItem text="Research" />
			<HeaderNavItem text="Ideas" />
		</HeaderNav>
		{/if}
	</Header>
	<SideNav fixed bind:isOpen={isSideNavOpen}>
		<!-- If the windows is small, push Nav links into SideNav-->
		{#if winWidth < 1056}
		<SideNavItems>
			<SideNavLink icon={iAccounts} text="Accounts" />
			<SideNavLink icon={iResearch} text="Research" />
			<SideNavLink icon={iIdeas} text="Ideas" />
		</SideNavItems>
		{/if}
	</SideNav>
</main>

<style>

</style>