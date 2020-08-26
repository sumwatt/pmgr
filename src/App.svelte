<script>
  import HNav from "./Layout/HNav.svelte";
  import HSideNav from "./Layout/HSideNav.svelte";
  import ContentLayout from "./Layout/ContentLayout.svelte"; 
import { Content } from "carbon-components-svelte";
  /**
   * 
   * 
   * 
   */
  let winWidth = undefined;
   /**
   * 
   * 
   * 
   */
  let isSideNavOpen = false;
   /**
   * 
   * 
   * 
   */
  let activeComponent = "Accounts";
</script>
<svelte:head>
  <link
    rel="stylesheet"
    href="https://unpkg.com/carbon-components/css/carbon-components.min.css"
  />
</svelte:head>

<svelte:window bind:innerWidth={winWidth} />

<main>
  <HNav winWidth={winWidth} bind:isSideNavOpen />
  <HSideNav bind:isSideNavOpen winWidth={winWidth} activeComponent={activeComponent}/>
  <ContentLayout {activeComponent}>
</main>

<style>

</style>
