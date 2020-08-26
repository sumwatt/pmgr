<script>
  import HNav from "./HNav.svelte";
  import HSideNav from "./HSideNav.svelte";
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
  let activeComponent = undefined;
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
</main>

<style>

</style>
