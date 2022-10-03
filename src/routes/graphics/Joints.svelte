<script>
  import SelJoint from "./SelJoint.svelte";
  import SelAxis from "./SelAxis.svelte";
  import OnlyAxis from "./OnlyAxis.svelte";
  import OnlyJoint from "./OnlyJoint.svelte";

  export let selection = null;
  let questions = [`Angles`, `Angular Velocity`];
  let Comcheck = false;

  export let Kcheck = false;
  export let Hcheck = false;
  export let Acheck = false;

  export let UPcheck = false;
  export let FBcheck = false;
  export let RLcheck = false;

  export let comments;
</script>

<div class="m-6 grid grow grid-cols-2  gap-8 rounded bg-white p-4 shadow-2xl">
  <div>
    {#if UPcheck && FBcheck}
      <OnlyJoint bind:Kcheck bind:Hcheck bind:Acheck />
    {:else if UPcheck && RLcheck}
      <OnlyJoint bind:Kcheck bind:Hcheck bind:Acheck />
    {:else if FBcheck && RLcheck}
      <OnlyJoint bind:Kcheck bind:Hcheck bind:Acheck />
    {:else if UPcheck && RLcheck && FBcheck}
      <OnlyJoint bind:Kcheck bind:Hcheck bind:Acheck />
    {:else}
      <SelJoint bind:Kcheck bind:Hcheck bind:Acheck />
    {/if}
    <div class="mt-8">
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
    {#if Acheck && Hcheck}
      <OnlyAxis bind:UPcheck bind:FBcheck bind:RLcheck />
    {:else if Acheck && Kcheck}
      <OnlyAxis bind:UPcheck bind:FBcheck bind:RLcheck />
    {:else if Kcheck && Hcheck}
      <OnlyAxis bind:UPcheck bind:FBcheck bind:RLcheck />
    {:else if Hcheck && Kcheck && Acheck}
      <OnlyAxis bind:UPcheck bind:FBcheck bind:RLcheck />
    {:else}
      <SelAxis bind:UPcheck bind:FBcheck bind:RLcheck />
    {/if}

    <div class="mt-14">
      <input
        id="default-checkbox"
        type="checkbox"
        bind:checked={Comcheck}
        class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600"
      />
      <label
        for="default-checkbox"
        class="ml-2 text-sm font-medium text-gray-900">Add Comments</label
      >
    </div>
  </div>
  {#if Comcheck}
    <div class="col-span-2">
      <label class="block">
        <span class="text-sm font-semibold">Comments</span>
        <textarea
          bind:value={comments}
          class="form-textarea mt-1 block w-full rounded border border-slate-400"
          rows="4"
          placeholder="Enter specialist comments."
        />
      </label>
    </div>
  {/if}
</div>
