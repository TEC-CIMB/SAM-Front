<script>
  let questions = [`Angles`, `Angular velocity`, `Both`];
  let choose = null;
</script>

<div class="flex grow flex-row">
  <div class="flex basis-1/3 flex-col bg-[#eaedf0]">
    <div class="grid justify-items-center">
      <div class="my-2 mt-24 text-gray-700">Select graphic:</div>
      <select bind:value={choose}>
        {#each questions as question}
          <option value={question}>
            {question}
          </option>
        {/each}
      </select>
    </div>
  </div>
  <div class="basis-1 bg-[#555353]" />
  <div class="grid grow basis-2/3 justify-items-center pt-5">
    {#if choose == "Angles"}
      <img class="w-78" src="exp.jpg" alt="example" />
    {:else if choose == "Angular velocity"}
      <img class="w-78" src="exmp2.jpg" alt="example" />
    {:else if (choose = "Both")}
      <div class="flex flex-col">
        <img class="w-78" src="exp.jpg" alt="example" />
        <img class="w-78" src="exmp2.jpg" alt="example" />
      </div>
    {:else}
      <h1 class="text-white">a</h1>
    {/if}
  </div>
</div>
