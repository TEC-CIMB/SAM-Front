<script>
  export let section;
</script>

<div class="flex grow flex-row justify-center">
  {#if section == "Lower section"}
    <div>
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Front view
        <img class="w-full" src="lw.svg" alt="low" />
      </div>
    </div>
    <div>
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Back view
        <img class="w-full" src="lw.svg" alt="low" />
      </div>
    </div>
  {:else if section == "Upper section"}
    <div class="flex grow flex-row justify-center">
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Front view
        <img class="w-full" src="up.svg" alt="up" />
      </div>
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Back view
        <img class="w-full" src="up.svg" alt="up" />
      </div>
    </div>
  {:else if section == "Full body"}
    <div class="flex grow justify-center">
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Front view
        <img class="w-full" src="full.svg" alt="fb" />
      </div>
      <div class="m-6 grid justify-items-center font-bold text-[#022352f1] ">
        Back view
        <img class="w-full" src="full.svg" alt="fb" />
      </div>
    </div>
  {/if}
</div>
