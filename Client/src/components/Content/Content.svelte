<script lang="ts">
    import Intro from './Intro.svelte'
    import Interests from './Interests.svelte'
    import Experience from './Experience.svelte'
    import Portfolio from './Portfolio.svelte'

  /* @todo make also mobile friendly */
    let name: string = 'Pepijn Hillemans';
    let description: string = 'IT student that likes experimenting';
</script>

<div class="p-10 bg-gray-200 space-y-4">
    <Intro {name} {description} />
    <Interests />
    <Experience />
    <Portfolio />
</div>
