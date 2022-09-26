<script>
  import "../app.css";
</script>

<div class="flex h-screen flex-col">
  <div
    class="flex w-full items-center gap-6 bg-[#022352e0] py-3 px-2 font-mono text-xl font-bold text-white"
  >
    <img class="h-12" src="2.png" alt="sensor" />
    <a href="/load" class="hover:text-yellow-300">Load files</a>
    <a href="/comments" class="hover:text-yellow-300">Add Comments</a>
    <a href="/help" class="hover:text-yellow-300">Help</a>
  </div>
  <div class="flex h-1 bg-[#555353] text-xs text-[#555353]">.</div>
  <slot />

  <div class="mt-auto bg-[#8a8b8c5f] py-1 px-2">
    <div class="font-mono">Produced by:</div>
    <img class="h-5" src="CIMB.png" alt="cimb logo" />
  </div>
</div>
<!-- 2c363f -->
