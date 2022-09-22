<script>
  import "../app.css";
</script>

<div class="flex h-screen flex-col">
  <div
    class="flex w-full items-center gap-6 bg-[#023c40] py-3 px-2 font-mono text-xl font-bold text-white"
  >
    <img class="h-12" src="2.png" alt="sensor" />
    <a href="/load" class="hover:text-yellow-300">Load files</a>
    <a href="/comments" class="hover:text-yellow-300">Add Comments</a>
    <a href="/help" class="hover:text-yellow-300">Help</a>
  </div>

  <slot />

  <div class="mt-auto bg-neutral-200 py-1 px-2">
    <div class="font-mono">Produced by:</div>
    <img class="h-5" src="CIMB.png" alt="sensor" />
  </div>
</div>
<!-- 2c363f -->
