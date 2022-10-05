<script>
  export let files;
  export let section = null;
  export let screen;
  let questions = [`Lower section`, `Upper section`, `Full body`];
</script>

<div class="m-6 flex grow flex-col rounded bg-white p-2 shadow-2xl">
  <div class="mt-6 ml-8 mr-16">
    <h3 class="mb-3 mt-3 text-sm font-bold">Choose and place the sensor</h3>
    {#each files as file}
      <div class="ml-2 w-full rounded border border-gray-200">
        <input
          id="RadioSensors"
          type="radio"
          value="S1"
          name="bordered-radio"
          class="ml-2 h-4 border-gray-300 bg-gray-100 text-blue-600"
        />
        <label for="RadioSensors" class="mt-2 text-sm font-medium text-gray-900"
          >{file.name}</label
        >
      </div>
    {/each}
  </div>

  <div class="m-10 flex flex-col items-center justify-center">
    <div class="mb-3 text-sm font-bold">Select a section:</div>
    <select class="bg-gray-200 shadow-2xl" bind:value={section}>
      {#each questions as question}
        <option value={question}>
          {question}
        </option>
      {/each}
    </select>
    {#if section !== null}
      <button
        on:click={() => {
          screen = "graphics";
        }}
        class="mt-10 flex justify-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
      >
        Show graphics
      </button>
    {/if}
  </div>
</div>
