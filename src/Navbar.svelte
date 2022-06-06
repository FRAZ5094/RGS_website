<script lang="ts">
  import NavMenuItems from "./NavMenuItems.svelte";
  let open=false;
  $: outerWidth = 0;
  $: innerWidth = 0;
  $: outerHeight = 0;
  $: innerHeight = 0;
  $:mobile = outerWidth <=768;

  $:{
    /*if open and changes to not mobile close*/
    if (!mobile && open){
      open = false;
    }
  }

  import { fade, blur, fly, slide, scale } from "svelte/transition";
  import { quintOut } from "svelte/easing";
</script>

<svelte:window bind:outerWidth bind:innerHeight bind:outerHeight />

<nav class="flex flex-row justify-evenly bg-primary items-center">
  <a href="https://www.instagram.com/rearglutespread_/?hl=en" class="p-4">
    <img src="/images/instagram.svg" class="h-16 md:hidden inline-flex"/>
  </a>
  <a class="" href="#">
    <img class="h-36 md:w-full" src="/images/RGS_logo.png" />
  </a>
  {#if !mobile}
  <NavMenuItems />
  {/if}
  <button class="p-4" on:click={() => open = !open}>
        <img src={open ? "/images/x.svg" : "/images/menu.svg"} class="h-16 md:hidden inline-flex" />
  </button>
</nav>
{#if open}
<NavMenuItems />
{/if}

<p>{outerWidth}</p>
<p>{mobile}</p>
