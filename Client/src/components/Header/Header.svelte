<script lang="ts">
    import NavItems from './NavItems.svelte';
    
    /* images */
    import github from '../../images/github.png';
    import linkedin from '../../images/linkedin.png';

    let width: number;
    $: tooSmall = (): boolean => {
        return width <= 1280;
    }
</script>

<svelte:window bind:innerWidth={width} />

<div class="fixed flex justify-around w-full h-16">
    {#if !tooSmall()}
        <div class="flex items-center justify-around inline-block w-3/5 text-center text-white bg-orange-700 rounded-b-lg">
            <NavItems {width}/>
            <div class="flex">
                <a href="https://www.github.com/phillemans" target="_blank" class="w-8 m-2 rounded-full hover:bg-orange-600 hover:shadow-inner hover:shadow-lg">
                    <img src={github} alt="github" />
                </a>
                <a href="https://www.linkedin.com/in/pepijn-hillemans-907114153/" target="_blank" class="w-8 m-2 rounded-full hover:bg-orange-600 hover:shadow-inner hover:shadow-lg">
                    <img src={linkedin} alt="linkedin" />
                </a>
            </div>
        </div>
    {:else}
        <div class="flex items-center justify-around inline-block w-full text-center text-white bg-orange-700">
            <NavItems {width}/>
            <div class="flex">
                <a href="https://www.github.com/phillemans" target="_blank" class="w-8 m-2 rounded-full hover:bg-orange-600 hover:shadow-inner hover:shadow-lg">
                    <img src={github} alt="github" />
                </a>
                <a href="https://www.linkedin.com/in/pepijn-hillemans-907114153/" target="_blank" class="w-8 m-2 rounded-full hover:bg-orange-600 hover:shadow-inner hover:shadow-lg">
                    <img src={linkedin} alt="linkedin" />
                </a>
            </div>
        </div>
    {/if}
</div>
