<script lang="ts">
    import Intro from './Intro.svelte'
    import Interests from './Interests.svelte'
    import Experience from './Experience.svelte'
    import Portfolio from './Portfolio.svelte'

    let name: string = 'Pepijn Hillemans';
    let description: string = 'IT student that likes experimenting';
</script>

<style style="css">
    .gigantisch {
        height: 1200px;
    }
</style>

<div class="bg-gray-200 gigantisch">
    <Intro {name} {description} />
    <Interests />
    <Experience />
    <Portfolio />
</div>
