<script lang="ts">
    import Textblock from './Textblock.svelte';
    import image from '../../../images/peppi.jpeg';

    let age: number = new Date().getFullYear() - new Date(2000, 2, 1).getFullYear();
</script>

<div class="flex w-3/5 bg-gray-100 rounded-lg">
    <!-- Name intro -->
    <div class="p-10">
        <Textblock {age} />
    </div>
        
    <div class="w-full rounded-lg">
        <img src={image} alt="thisimage" class="w-full border-2 border-orange-500 border-solid rounded-lg">
    </div>
</div>
