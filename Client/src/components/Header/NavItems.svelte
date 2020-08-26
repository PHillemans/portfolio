<script lang="ts">
  import type {navigation} from './header';
  import Link from '../extra/Link.svelte';

  export let width:number;

  /* @todo make interactive */
  let topItem: boolean = false;
  let lastItem: boolean = false;

  let navigateItems: navigation[] = [
    {name: 'Introduction'},
    {name: 'Interests', selected: false},
    {name: 'Experience'},
    {name: 'Portfolio'}
  ];

  //todo check if item is last item or first
  let getNavigateItem = (index: number): string => {
    let navigateItemIndex = index > navigateItems.length-1 ? index-navigateItems.length : index;
    return navigateItems[navigateItemIndex].name;
  }

  let currentItem: navigation = navigateItems.filter((item: navigation) => {
    return item.name == 'Portfolio';
  })[0];

  let prevItem = getNavigateItem(navigateItems.findIndex((navigateItem: navigation) => {
    return currentItem.name == navigateItem.name;
  })-1);

  let nextItem = getNavigateItem(navigateItems.findIndex((navigateItem: navigation) => {
    return currentItem.name == navigateItem.name;
  })+1);

  $: fits = () => {
    return width >= 700;
  }

</script>

<!-- On larger screens  -->
{#if fits()}
  <div class="flex text-xl">
    {#each navigateItems as {name, selected}}
      <Link buttonName={name} {selected} />
    {/each}
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

