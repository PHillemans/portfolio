<script lang="ts">
  import Link from '../extra/Link.svelte';

  export let width:number;

  $: fits = () => {
    return width >= 700;
  }

  /* @todo make interactive */
  let topItem: boolean = false;
  let lastItem: boolean = false;
  let currentItem: string = 'Introduction';
</script>

<!-- On larger screens  -->
{#if fits()}
  <div class="flex text-xl">
    <Link buttonName={"Introduction"} />
    <Link buttonName={"Interests"} />
    <Link buttonName={"Experience"} />
    <Link buttonName={"Portfolio"} />
  </div>
{:else}
  <div class="flex justify-center w-full">

    {#if !topItem}
      <div class="px-3 py-2 text-orange-200 border-2 border-orange-600 border-solid rounded-lg cursor-pointer active:text-orange-600 active:bg-orange-800">
        {"<"}
      </div>
    {/if}

    <div class="p-2 text-orange-200 border-2 border-transparent">{currentItem}</div>

    {#if !lastItem}
      <button class="px-3 py-2 text-orange-200 border-2 border-orange-600 border-solid rounded-lg cursor-pointer active:text-orange-600 active:bg-orange-800">
        {">"}
      </button>
    {/if}

  </div>
{/if}

