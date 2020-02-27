<script>
  export let page;

  import { Link } from "yrv";

  import HeaderLink from "../components/HeaderLink.svelte";
  import HamburgerButton from "../components/HamburgerButton.svelte";

  let showSideBar = false;

  function toggleSideBar() {
    showSideBar = !showSideBar;
  }
</script>

<style>
  .slide {
    transition: 0.5s;
  }
</style>

<header class="bg-gray-900 h-16 flex shadow-md">
  <div class="w-1/4 md:hidden cursor-pointer">
    <HamburgerButton on:message={toggleSideBar} />

    <div
      class="absolute left-0 top-0 w-3/4 h-full bg-gray-700 slide "
      style={showSideBar ? '' : 'left: -75%;'}>
      <HamburgerButton on:message={toggleSideBar} />
      <HeaderLink link="" text="Home" {page} align="left" />
      <HeaderLink link="climbers" text="The Climbers" {page} align="left"/>
      <HeaderLink link="routes" text="The Routes" {page} align="left"/>
      <HeaderLink link="mission" text="The Mission" {page} align="left"/>
    </div>
  </div>

  <div class="hidden md:flex w-full align-middle">
    <Link href="/">
      <img src="images/logo.png" class="w-12 h-8 m-4" />
    </Link>
    <HeaderLink link="climbers" text="The Climbers" {page} />
    <HeaderLink link="routes" text="The Routes" {page} />
    <HeaderLink link="mission" text="The Mission" {page} />
  </div>
</header>
