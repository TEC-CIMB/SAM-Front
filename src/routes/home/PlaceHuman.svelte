<script>
  export let section;
</script>

{#if section == "Lower Section"}
  <div class="ml-24 mr-24 mt-5 flex justify-evenly">
    <img class="h-screen w-full" src="Low.svg" alt="lower" />
  </div>
{:else if section == "Upper Section"}
  <div class="flex items-center justify-center">
    <img src="Upper.svg" alt="upper" />
  </div>
{:else if section == "Full Body"}
  <div class="ml-24 mr-24 mt-5 flex justify-evenly">
    <img class="h-screen w-full" src="Full.svg" alt="Full" />
  </div>
{/if}
