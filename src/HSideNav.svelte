<script>
    import { 
        SideNav,
        SideNavItems,	
        SideNavLink
    } from "carbon-components-svelte";

    import Finance32 from "carbon-icons-svelte/lib/Finance32";
    import Idea32 from "carbon-icons-svelte/lib/Idea32";
    import Microscope32 from "carbon-icons-svelte/lib/Microscope32";
    import Settings32 from "carbon-icons-svelte/lib/Settings32";
    import Help32 from "carbon-icons-svelte/lib/Help32";

    /**
     * Icon objects
     */
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

    let iSettings = {
        class: undefined,
        skeleton: false,
        render: Settings32,
        title: "Settings",
        tabindex: "0",
        focusable: false,
        style: undefined
    }

    let iHelp = {
        class: undefined,
        skeleton: false,
        render: Help32,
        title: "Help",
        tabindex: "0",
        focusable: false,
        style: undefined
    }
    export let isSideNavOpen = false;
    export let winWidth = undefined;
</script>

<SideNav fixed bind:isOpen={isSideNavOpen}>
    <!-- If the windows is small, push Nav links into SideNav-->
    {#if winWidth < 1056}
    <SideNavItems>
        <SideNavLink icon={iAccounts} text="Accounts" />
        <SideNavLink icon={iResearch} text="Research" />
        <SideNavLink icon={iIdeas} text="Ideas" />
        <hr />
        <SideNavLink icon={iSettings} text="Settings" />
        <SideNavLink icon={iHelp} text="Help" />
    </SideNavItems>
    {/if}
</SideNav>