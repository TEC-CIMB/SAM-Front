<script>
  export let files;
  let selected;
  let questions = [`Lower section`, `Upper section`, `Full body`];
</script>

<div class="flex grow flex-row">
  <div class="flex basis-1/4 bg-[#eaedf0]">
    <div class="m-5 bg-white p-5">
      {#each files as file}
        <div>
          <input
            id="RadioSensors"
            type="radio"
            value="S1"
            name="bordered-radio"
            class="h-4 w-4 border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500 dark:border-gray-600 dark:bg-gray-700 dark:ring-offset-gray-800 dark:focus:ring-blue-600"
          />
          <label
            for="RadioSensors"
            class="ml-2 text-sm font-medium text-gray-900 dark:text-gray-300"
            >{file.name}</label
          >
        </div>
      {/each}
    </div>
    <div class="flex flex-col items-center justify-evenly">
      <div class=" text-gray-700">Select a section:</div>
      <select bind:value={selected}>
        {#each questions as question}
          <option value={question}>
            {question}
          </option>
        {/each}
      </select>
    </div>
  </div>
  <div class="flex basis-1 bg-[#555353]" />
  <div class="flex basis-3/4 bg-white">monachos</div>
</div>
