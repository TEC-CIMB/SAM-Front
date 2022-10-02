<script>
  import "../app.css";
</script>

<div class="flex h-screen flex-col">
  <div class="flex flex-row items-center justify-between  bg-[#022352ca] p-2">
    <img class="h-12 px-7" src="2.png" alt="sensor" />
    <div class="flex flex-row gap-6 pr-5 font-bold text-white">
      <a href="/home">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-home hover:fill-white hover:stroke-[#022352]"
          ><path d="M3 9l9-7 9 7v11a2 2 0 0 1-2 2H5a2 2 0 0 1-2-2z" /><polyline
            points="9 22 9 12 15 12 15 22"
          /></svg
        >
      </a>
      <a href="/save">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-save hover:fill-white hover:stroke-[#022352]"
          ><path
            d="M19 21H5a2 2 0 0 1-2-2V5a2 2 0 0 1 2-2h11l5 5v11a2 2 0 0 1-2 2z"
          /><polyline points="17 21 17 13 7 13 7 21" /><polyline
            points="7 3 7 8 15 8"
          /></svg
        >
      </a>
      <a href="/help">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="32"
          height="32"
          viewBox="0 0 24 24"
          fill="none"
          stroke="currentColor"
          stroke-width="2"
          stroke-linecap="round"
          stroke-linejoin="round"
          class="feather feather-help-circle hover:fill-white hover:stroke-[#022352]"
          ><circle cx="12" cy="12" r="10" /><path
            d="M9.09 9a3 3 0 0 1 5.83 1c0 2-3 3-3 3"
          /><line x1="12" y1="17" x2="12.01" y2="17" /></svg
        >
      </a>
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
