<script lang="ts">
    export let name: string;
    export let description: string;
</script>

<div class="flex justify-between">
    <!-- Name intro -->
    <div class="flex-row items-center justify-center w-2/5 pt-20 mt-20 text-gray-600">
        <div class="flex-col p-3 text-center text-orange-400">
            <span class="block lg:text-6xl md:text-lg md:font-bold">{name}</span>
            <span class="block font-thin text-gray-800 md:text-xs text-md">{description}</span>
        </div>
        <div>
            <div class="p-5 m-6 bg-gray-100 rounded-lg">
                Hey thr, I am an IT studnt from Hoogrhid, Th Nthrlands. Studying at Hz univrsity of applid scincs.
            </div>
        </div>
    </div>
    <!-- 2nd part with techniques used and who I am -->
    <div class="flex-row w-1/2 p-5 mt-24 mr-20 bg-gray-200 rounded-lg">
        <div>
            <span class="font-semibold text-gray-500">
                This website is crafted using:
            </span>
            <div>
            </div>
        </div>
    </div>
</div>
