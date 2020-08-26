<script lang="ts">
  import Intro from './Intro.svelte'
  import Interests from './Interests.svelte'
  import Experience from './Experience.svelte'
  import Portfolio from './Portfolio.svelte'

  /* @todo make also mobile friendly */
  let name: string = 'Pepijn Hillemans';
  let description: string = 'Experimenting to find my passion';
  let width:number;
</script>

<svelte:window bind:innerWidth={width} />

<div class="justify-around flex flex-wrap {width > 700 ? 'p-10':'pt-10'} space-y-4">
  <Intro {name} {description} />
  <Interests />
  <Experience />
  <Portfolio />
</div>
