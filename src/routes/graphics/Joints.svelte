<script>
  import SelJoint from "./SelJoint.svelte";
  import SelAxis from "./SelAxis.svelte";

  export let selection = null;
  let questions = [`Angles`, `Angular Velocity`];
  let check = false;
</script>

<div class="m-6 grid grow grid-cols-2  gap-8 rounded bg-white p-4 shadow-2xl">
  <div>
    <SelJoint />
    <div class="mt-14">
      <div class="text-sm font-bold">Select a graphic:</div>
      <select class="bg-gray-200 shadow-2xl" bind:value={selection}>
        {#each questions as question}
          <option value={question}>
            {question}
          </option>
        {/each}
      </select>
    </div>
  </div>
  <div>
    <SelAxis />
    <div class="mt-20">
      <input
        id="default-checkbox"
        type="checkbox"
        bind:checked={check}
        class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600"
      />
      <label
        for="default-checkbox"
        class="ml-2 text-sm font-medium text-gray-900">Add Comments</label
      >
    </div>
  </div>
  {#if check}
    <div class="col-span-2 mt-2">
      <label class="block">
        <span class="text-sm font-semibold">Comments</span>
        <textarea
          class="form-textarea mt-1 block w-full rounded border border-slate-400"
          rows="5"
          placeholder="Enter specialist comments."
        />
      </label>
    </div>
  {/if}
</div>
