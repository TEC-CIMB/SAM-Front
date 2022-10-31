<script>
  import Lower from "./Lower.svelte";
  import Upper from "./Upper.svelte";
  import Full from "./Full.svelte";

  export let files;
  export let section = null;
  export let screen;
  let sensor = [];
</script>

<div class="m-6 flex grow flex-col rounded bg-white shadow-2xl">
  <div class="mt-6 ml-8 mr-16 items-center justify-center">
    <h3 class="mb-2 text-lg font-medium text-gray-900 dark:text-white">
      Select a section:
    </h3>
    <ul class="grid w-full grid-cols-1 gap-2">
      <li>
        <input
          type="radio"
          id="Low"
          name="hosting"
          class="peer hidden"
          required
        />
        <label
          on:click={() => {
            section = "Lower Section";
          }}
          for="Low"
          class="inline-flex w-full cursor-pointer items-center justify-between rounded-lg border border-gray-200 bg-white p-2 text-gray-500 hover:bg-gray-100 hover:text-gray-600 peer-checked:border-blue-600 peer-checked:text-blue-600"
        >
          <div class="w-full">Lower Section</div>
        </label>
      </li>
      <li>
        <input type="radio" id="Up" name="hosting" class="peer hidden" />
        <label
          on:click={() => {
            section = "Upper Section";
          }}
          for="Up"
          class="inline-flex w-full cursor-pointer items-center justify-between rounded-lg border border-gray-200 bg-white p-2 text-gray-500 hover:bg-gray-100 hover:text-gray-600 peer-checked:border-blue-600 peer-checked:text-blue-600"
        >
          <div class="w-full">Upper Section</div>
        </label>
      </li>
      <li>
        <input type="radio" id="Full" name="hosting" class="peer hidden" />

        <label
          on:click={() => {
            section = "Full Body";
          }}
          for="Full"
          class="inline-flex w-full cursor-pointer items-center justify-between rounded-lg border border-gray-200 bg-white p-2 text-gray-500 hover:bg-gray-100 hover:text-gray-600 peer-checked:border-blue-600 peer-checked:text-blue-600"
        >
          <div class="w-full">Full Body</div>
        </label>
      </li>
    </ul>
  </div>
  <div class="mt-6 flex flex-col gap-3">
    {#if section !== null}
      {#if section == "Lower Section"}
        <Lower {files} bind:sensor />
      {:else if section == "Upper Section"}
        <Upper {files} bind:sensor />
      {:else if section == "Full Body"}
        <Full {files} bind:sensor />
      {/if}

      {#if sensor.includes("Select")}
        <button
          class="mt-10 mb-8 flex w-48 cursor-not-allowed justify-center self-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259] "
        >
          Show graphics
        </button>
      {:else}
        <button
          on:click={() => {
            screen = "graphics";
          }}
          class="mt-10 mb-8 flex w-48 justify-center self-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
        >
          Show graphics
        </button>
      {/if}
    {/if}
  </div>
</div>
