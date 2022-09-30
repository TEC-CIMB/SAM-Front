<script>
  import "../app.css";
</script>

<div class="flex h-screen flex-col">
  <div class="flex flex-row items-center justify-between  bg-[#022352e0] p-2">
    <img class="h-12 px-7" src="2.png" alt="sensor" />
    <div
      class="flex flex-row gap-6 pr-5 font-mono text-xl font-bold text-white"
    >
      <a href="/home" class="hover:text-yellow-300 ">Home</a>
      <a href="/save" class="hover:text-yellow-300">Save</a>
      <a href="/help" class="hover:text-yellow-300">Help</a>
    </div>
  </div>
  <div class="flex h-1 bg-[#555353] text-xs text-[#555353]">.</div>
  <slot />

  <div class="mt-auto bg-[#8a8b8c5f] py-1 px-2">
    <div class="font-mono">Produced by:</div>
    <div class="flex flex-row">
      <img class="h-5" src="CIMB.png" alt="cimb logo" />
      <h1 class="px-2">2022</h1>
    </div>
  </div>
</div>
<!-- 2c363f -->
