<script>
  let questions = [
    `R Shoulder`,
    `R Bicep`,
    `R Forearm`,
    `R Hand`,
    `R Scapula`,
    `L Shoulder`,
    `L Bicep`,
    `L Forearm`,
    `L Hand`,
    `L Scapula`,
    `Thoracic`,
    `Lumbar`,
  ];
  export let files;
  export let sensor = Array(files.lenght);
</script>

<h2 class="mb-2 ml-8">Select the sensor location</h2>
<div
  class="ml-16 mr-16 flex flex-col justify-center gap-2 rounded border shadow"
>
  {#each files as file, i}
    <div class="ml-4 mt-1 text-sm font-medium text-gray-900">{file.name}</div>
    <select
      class="ml-8 mr-8 mb-2 bg-gray-200 shadow-2xl"
      bind:value={sensor[i]}
    >
      <option disabled selected>Select</option>
      {#each questions as question}
        <option value={question}>
          {question}
        </option>
      {/each}
    </select>
  {/each}
</div>
