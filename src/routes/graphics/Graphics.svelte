<script>
  import SelGrap from "./SelGrap.svelte";
  import Joints from "./Joints.svelte";
  export let selection = null;
  export let comments = null;
</script>

<div class="flex grow">
  <div class="flex basis-1/3 bg-[#eaedf0]">
    <Joints bind:selection bind:comments />
  </div>
  <div class="flex basis-1 bg-[#555353]" />
  <SelGrap {selection} />
  <div class="flex grow basis-2/3 bg-white" />
</div>
