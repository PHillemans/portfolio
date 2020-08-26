<script lang="ts">
  import Textblock from './Textblock.svelte';
  import image from '../../../images/peppi.jpeg';

  let age: number = new Date().getFullYear() - new Date(2000, 2, 1).getFullYear();
  let width:number;

  $: classes = [
    width > 1800 ? 'w-1/2':'w-4/5',
    width > 700 ? 'text-lg':'text-sm',
  ];

</script>
<svelte:window bind:innerWidth={width} />

{#if width < 1200}
  <div class="shadow-inner flex-col flex {classes.join(' ')} items-center bg-indigo-200 rounded-lg">
    <img src={image} alt="thisimage" class="w-48 mt-5 border-2 border-orange-500 border-solid rounded-full"/>
    <!-- Name intro -->
    <div class="p-2">
      <Textblock {age} />
    </div>

  </div>
{:else}
  <div class="flex shadow-inner shadow-lg {classes.join(' ')} items-center bg-indigo-200 rounded-lg">
    <!-- Name intro -->
    <div class="p-10">
      <Textblock {age} />
    </div>

    <div class="rounded-lg ">
      <img src={image} alt="thisimage" style="width: {width/2}px;" class="border-2 border-orange-500 border-solid rounded-l-lg "/>
    </div>
  </div>
{/if}
