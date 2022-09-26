<script>
  let st = "Load files";
  let Cstate = () => (st = "Loaded");
</script>

<div class="flex grow">
  <div class="flex basis-1/3 flex-col bg-[#eaedf0]">
    <div class="grid justify-items-center py-5">
      <img class="w-28" src="load.svg" alt="load" />
    </div>
    <div class="grid justify-items-center">
      <button
        on:click={Cstate}
        class="rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
        >{st}
      </button>
    </div>
    {#if st == "Loaded"}
      <div class="grid justify-items-center">
        <div class="relative my-24 inline-block w-48">
          <select
            class="focus:shadow-outline block w-full appearance-none rounded border border-[#022352b9] bg-white px-4 py-2 pr-8 leading-tight shadow hover:border-[#022352] focus:outline-none"
          >
            <option>Select section</option>
            <option>Lower section</option>
            <option>Upper section</option>
            <option>Full body</option>
          </select>
          <div
            class="pointer-events-none absolute inset-y-0 right-0 flex items-center px-2 text-gray-700"
          >
            <svg
              class="h-4 w-4 fill-current"
              xmlns="http://www.w3.org/2000/svg"
              viewBox="0 0 20 20"
              ><path
                d="M9.293 12.95l.707.707L15.657 8l-1.414-1.414L10 10.828 5.757 6.586 4.343 8z"
              /></svg
            >
          </div>
        </div>
      </div>
    {:else}
      <div class="flex basis-3/4 text-[#eaedf0] ">no</div>
    {/if}
  </div>
  <div class="basis-1 bg-[#555353]" />
  <div class="basis-2/3 ">02</div>
</div>
