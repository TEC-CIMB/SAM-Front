<script>
  import Custom from "./Custom.svelte";
  import PlaceHuman from "./PlaceHuman.svelte";
  export let files;
  let section;
</script>

<div class="flex grow">
  <div class="flex basis-1/3 bg-[#eaedf0]">
    <Custom {files} bind:section />
  </div>
  <div class="flex basis-1 bg-[#555353]" />
  <div class="flex grow basis-2/3 bg-white">
    <PlaceHuman {section} />
  </div>
</div>
