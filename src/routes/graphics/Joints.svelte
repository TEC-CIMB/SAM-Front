<script>
  import SelJoint from "./SelJoint.svelte";
  import SelAxis from "./SelAxis.svelte";
</script>

<div
  class="m-6 grid grow grid-cols-2 justify-items-stretch gap-8 bg-white p-4 shadow-2xl"
>
  <div>
    <SelJoint />
  </div>
  <div>
    <SelAxis />
  </div>
</div>
