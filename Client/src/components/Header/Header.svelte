<script lang="ts">
    import Link from '../extra/Link.svelte';
    import Seperator from '../extra/Seperator.svelte';
</script>

<div class="fixed flex justify-end w-full h-16">
  <div class="flex items-center content-around
  justify-center inline-block w-3/5
  text-center text-white bg-orange-700 rounded-bl-lg ">
        <div class="flex text-center lg:text-2xl md:text-lg">
            <Link buttonName={"Introduction"} />
            <Seperator sep={"/"} />
            <Link buttonName={"Interests"} />
            <Seperator  sep={"|"} />
            <Link buttonName={"Experience"} />
            <Seperator sep={"\\"} />
            <Link buttonName={"Portfolio"} />
        </div>
    </div>
</div>
