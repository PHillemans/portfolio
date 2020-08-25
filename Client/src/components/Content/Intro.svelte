<script lang="ts">
    import Information from './intro/Information.svelte';

    export let name: string;
    export let description: string;
</script>

<div class="flex-col pt-4 mt-10 text-center text-orange-400">
    <span class="text-4xl md:font-bold">{name}</span>
    <span class="block font-thin text-gray-800 md:text-xs text-md">{description}</span>
</div>
<div class="flex justify-center">
    <Information />
</div>
