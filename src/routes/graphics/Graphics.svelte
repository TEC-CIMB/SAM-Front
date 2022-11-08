<script>
  import SelGrap from "./SelGrap.svelte";
  import Joints from "./Joints.svelte";
  export let selection = null;
  export let comments = null;

  export let Kcheck = false;
  export let Hcheck = false;
  export let Acheck = false;

  export let UPcheck = false;
  export let FBcheck = false;
  export let RLcheck = false;
</script>

<div class="flex grow">
  <div class="flex basis-1/3 bg-[#eaedf0]">
    <Joints
      bind:selection
      bind:comments
      bind:Kcheck
      bind:Hcheck
      bind:Acheck
      bind:UPcheck
      bind:FBcheck
      bind:RLcheck
    />
  </div>
  <div class="flex basis-1 bg-[#555353]" />

  <div class="flex grow basis-2/3 bg-white">
    <SelGrap
      {selection}
      {Kcheck}
      {Hcheck}
      {Acheck}
      {UPcheck}
      {FBcheck}
      {RLcheck}
    />
  </div>
</div>
