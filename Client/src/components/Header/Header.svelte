<script lang="ts">
    import Link from '../extra/Link.svelte';
    import Seperator from '../extra/Seperator.svelte';
    import image from '../../images/peppi.jpeg';
</script>

<div class="fixed flex justify-around w-full h-16">
    <div class="flex items-center content-between justify-between inline-block w-4/5 text-center text-white bg-orange-700 rounded-b-lg ">
        <div>
            <img src={image} alt="thisimage" class="w-48 h-48 mt-20 bg-green-200 rounded-full">
        </div>
        <div class="flex text-center lg:text-2xl md:text-lg">
            <Link buttonName={"Introduction"} />
            <Seperator sep={"/"} />
            <Link buttonName={"Interests"} />
            <Seperator  sep={"|"} />
            <Link buttonName={"Experience"} />
            <Seperator sep={"\\"} />
            <Link buttonName={"Portfolio"} />
        </div>
        <div class="flex">
            <div class="w-8 h-8 m-2 bg-red-300 rounded-full hover:bg-red-400 hover:shadow-inner hover:shadow-lg"></div>
            <div class="w-8 h-8 m-2 bg-red-300 rounded-full hover:bg-red-400 hover:shadow-inner hover:shadow-lg"></div>
            <div class="w-8 h-8 m-2 bg-red-300 rounded-full hover:bg-red-400 hover:shadow-inner hover:shadow-lg"></div>
        </div>
    </div>
</div>
