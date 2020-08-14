<script lang="ts">
    import Intro from './Intro.svelte'
    import Interests from './Interests.svelte'
    import Experience from './Experience.svelte'
    import Portfolio from './Portfolio.svelte'
    let name:string = 'Pepijn Hillemans';
</script>

<style style="css">
    .gigantisch {
        height: 1200px;
    }
</style>

<div class='gigantisch'>
    <Intro name={name} />
    <Interests />
    <Experience />
    <Portfolio />
</div>
