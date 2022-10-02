<script>
  export let files;
  export let section = null;
  let questions = [`Lower section`, `Upper section`, `Full body`];
</script>

<div class="m-6 flex grow flex-col items-center bg-white p-2 shadow-2xl">
  <div>
    <h3 class="mb-3 mt-3 text-sm font-bold">Choose and place the sensor</h3>
    {#each files as file}
      <div class="mt-2">
        <input
          id="RadioSensors"
          type="radio"
          value="S1"
          name="bordered-radio"
          class="h-4 border-gray-300 bg-gray-100 text-blue-600"
        />
        <label for="RadioSensors" class="mt-2 text-sm font-medium text-gray-900"
          >{file.name}</label
        >
      </div>
    {/each}
  </div>

  <div class="m-8 flex flex-col">
    <div class="m-4 mb-3 mt-3 text-sm font-bold">Select a section:</div>
    <select class="bg-gray-200 shadow-2xl" bind:value={section}>
      {#each questions as question}
        <option value={question}>
          {question}
        </option>
      {/each}
    </select>
  </div>
  {#if section !== null}
    <a
      class="m-5 flex justify-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
      href="/graphics"
    >
      Show graphics
    </a>
  {/if}
</div>
