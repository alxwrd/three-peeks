<script>

export let page;

import { Link } from 'yrv';

import HeaderLink from '../components/HeaderLink.svelte'

</script>

<header class="bg-gray-900 h-16 flex shadow-md">
  <div class="w-1/4 p-4 md:hidden cursor-pointer">
    <svg
      class="fill-current text-white h-8 w-8"
      xmlns="http://www.w3.org/2000/svg"
      viewBox="0 0 20 20">
      <path
        d="M16.4 9H3.6c-.552 0-.6.447-.6 1 0 .553.048 1 .6 1h12.8c.552 0
        .6-.447.6-1 0-.553-.048-1-.6-1zm0 4H3.6c-.552 0-.6.447-.6 1 0 .553.048 1
        .6 1h12.8c.552 0 .6-.447.6-1 0-.553-.048-1-.6-1zM3.6 7h12.8c.552 0
        .6-.447.6-1 0-.553-.048-1-.6-1H3.6c-.552 0-.6.447-.6 1 0 .553.048 1 .6
        1z" />
    </svg>
  </div>


  <div class="hidden md:flex w-full align-middle">
    <Link href="/">
      <img src="images/logo.png" class="w-12 h-8 m-4" />
    </Link>
    <HeaderLink link="climbers" text="The Climbers" page={page}></HeaderLink>
    <HeaderLink link="routes" text="The Routes" page={page}></HeaderLink>
    <HeaderLink link="mission" text="The Mission" page={page}></HeaderLink>
  </div>
</header>