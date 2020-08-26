<script>

    import { 
        Header,
        HeaderNav,
        HeaderNavItem,
    } from "carbon-components-svelte";
    
    /**
     * @type {boolean} 
     */
    export let isSideNavOpen = false;
    
    /**
     * Holds the window width to handle resizing and menus 
     * @type {integer} 
     */
    export let winWidth = undefined;



</script>

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

