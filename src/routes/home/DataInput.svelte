<script>
  export let step = "input";
  let st = "Load files";
  let Cstate = () => {
    st = "Loaded";
    let reader = new FileReader();
  };
  let filesClick;
  export let files = [];
  export let name;
  export let date;
  export let test;
  export let age;
  export let weight;
  export let height;
  export let gender;
</script>

<div class="grow bg-[#eaedf0] px-44 py-44 pt-10 pb-10">
  <form class="grid grid-cols-2 gap-6 rounded bg-white p-8 shadow-md">
    <div class="mb-2">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="date">
        Date
      </label>
      <input
        bind:value={date}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="date"
        type="text"
        placeholder="dd/mm/aaaa"
      />
    </div>
    <div class="mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="test">
        Test Name
      </label>
      <input
        bind:value={test}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="test"
        type="text"
        placeholder="Flexion-Extension"
      />
    </div>
    <div class="col-span-2 col-start-1 mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="user">
        Patient Name
      </label>
      <input
        bind:value={name}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="user"
        type="text"
        placeholder="Jane Doe"
      />
    </div>
    <div class="col-start-1 mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="age">
        Age
      </label>
      <input
        bind:value={age}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="age"
        type="text"
      />
    </div>
    <div class="mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="gender">
        Gender
      </label>
      <input
        bind:value={gender}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="gender"
        type="text"
      />
    </div>
    <div class="col-start-1 mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="weight">
        Weight
      </label>
      <input
        bind:value={weight}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="weight"
        type="text"
      />
    </div>
    <div class="mb-1">
      <label class="mb-1 block text-sm font-bold text-gray-700" for="height">
        Height
      </label>
      <input
        bind:value={height}
        class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
        id="height"
        type="text"
      />
    </div>
  </form>
  <div class="mt-8 grid grid-cols-2 justify-items-center">
    <div>
      <button
        on:click={() => {
          filesClick.click();
        }}
        class=" h-8 w-32 rounded bg-[#022352e0] font-bold text-white hover:bg-[#02235259]"
        >{st}</button
      >
      <input
        bind:this={filesClick}
        bind:files
        multiple
        type="file"
        class="hidden"
        on:change={Cstate}
      />
    </div>

    <div class="grid justify-items-center">
      {#if st == "Loaded"}
        <button
          on:click={() => {
            step = "section";
          }}
          class="flex h-8 w-32 justify-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
          >Save</button
        >
      {:else}
        <button
          class="flex h-8 w-32 cursor-not-allowed justify-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
          >Save
        </button>
      {/if}
    </div>
  </div>
</div>
