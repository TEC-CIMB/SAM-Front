<script>
  let st = "Load files";
  let Cstate = () => {
    let reader = new FileReader();
    st = "Loaded";
  };
  let questions = [`Lower section`, `Upper section`, `Full body`];
  let selected;
  let filesClick;
  let files = [];
</script>

<div class="flex grow">
  <div class="flex basis-1/3 flex-col bg-[#eaedf0]">
    <div class="m-4 grid grid-cols-2 justify-items-center gap-4">
      <form class="rounded bg-white px-4 pt-4 pb-4 shadow-md">
        <div class="mb-2">
          <label
            class="mb-1 block text-sm font-bold text-gray-700"
            for="username"
          >
            Patient Name
          </label>
          <input
            class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
            id="username"
            type="text"
            placeholder="Jane Doe"
          />
        </div>
        <div class="mb-1">
          <label class="mb-1 block text-sm font-bold text-gray-700" for="test">
            Test Name
          </label>
          <input
            class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
            id="test"
            type="text"
            placeholder="Flexion-Extension"
          />
        </div>
      </form>
      <div class="flex flex-col items-center justify-center">
        <img class="w-24" src="load.svg" alt="load" />

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
      {#if st == "Loaded"}
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
        <div
          class=" m-4 flex flex-col justify-evenly gap-4  rounded border bg-white p-3"
        >
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
      {/if}
    </div>

    {#if st == "Loaded"}
      <div class="mt-8 grid justify-items-center">
        <a
          href="/graphics"
          class="rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259]"
          >Show graphics</a
        >
      </div>
    {:else}
      <div class="flex basis-3/4 text-[#eaedf0] " />
    {/if}
  </div>
  <div class="basis-1 bg-[#555353]" />
  {#if selected == "Lower section"}
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Front view
      <img class="w-78" src="lw.svg" alt="low" />
    </div>
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Back view
      <img class="w-78" src="lw.svg" alt="low" />
    </div>
  {:else if selected == "Upper section"}
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Front view
      <img class="w-78" src="up.svg" alt="up" />
    </div>
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Back view
      <img class="w-78" src="up.svg" alt="up" />
    </div>
  {:else if selected == "Full body"}
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Front view
      <img class="w-78" src="full.svg" alt="fb" />
    </div>
    <div
      class="mt-3 grid basis-1/3 justify-items-center font-bold text-[#022352f1] "
    >
      Back view
      <img class="w-78" src="full.svg" alt="fb" />
    </div>
  {/if}
</div>
