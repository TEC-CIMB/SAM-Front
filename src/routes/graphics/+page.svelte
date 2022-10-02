<script>
  import SelGrap from "./SelGrap.svelte";
  import Joints from "./Joints.svelte";
</script>

<div class="flex grow">
  <div class="flex basis-1/3 bg-[#eaedf0]">
    <Joints />
  </div>
  <div class="flex basis-1 bg-[#555353]" />
  <SelGrap />
  <div class="flex grow basis-2/3 bg-white" />
</div>
