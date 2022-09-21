<script>
  import "../app.css";
</script>

<div class="flex h-screen flex-col">
  <div
    class="flex w-full items-center gap-6 bg-cyan-800 py-3 px-2 font-mono font-bold text-white"
  >
    <img class="h-12" src="2.png" alt="sensor" />
    <a href="/cargar" class="hover:text-yellow-300">Load files</a>
    <button class="hover:text-yellow-300">Add Comments</button>
    <button class="hover:text-yellow-300">Help</button>
  </div>

  <slot />

  <div class="mt-auto bg-neutral-200 py-1 px-2">
    <div class="font-mono">Produced by:</div>
    <img class="h-5" src="CIMB.png" alt="sensor" />
  </div>
</div>
