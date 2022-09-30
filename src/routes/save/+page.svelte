<script>
</script>

<div class="grid grow grid-cols-4 gap-4 bg-[#eaedf0]">
  <div class="grid w-full max-w-xs justify-items-center">
    <form class="mb-4 rounded bg-white px-8 pt-6 pb-8 shadow-md">
      <div class="mb-4">
        <label
          class="mb-2 block text-sm font-bold text-gray-700"
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
      <div class="mb-6">
        <label class="mb-2 block text-sm font-bold text-gray-700" for="doct">
          Specialist Name
        </label>
        <input
          class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
          id="doct"
          type="text"
          placeholder="Joe Doe"
        />
      </div>
      <div class="mb-4">
        <label
          class="mb-2 block text-sm font-bold text-gray-700"
          for="comments"
        >
          Comments
        </label>
        <input
          class="focus:shadow-outline w-full appearance-none rounded border py-2 px-3 leading-tight text-gray-700 shadow focus:outline-none"
          id="comments"
          type="text"
          placeholder="Comments"
        />
      </div>
    </form>
  </div>
  <div>
    <img class="w-78" src="exp.jpg" alt="example" />
  </div>
  <div class=" w-9 ">
    <button
      class="inline-flex items-center rounded bg-gray-300 py-2 px-4 font-bold text-[#022352] hover:bg-gray-400"
    >
      <svg
        class="mr-2 h-4 w-4 fill-current"
        xmlns="http://www.w3.org/2000/svg"
        viewBox="0 0 20 20"
        ><path d="M13 8V2H7v6H2l8 8 8-8h-5zM0 18h20v2H0v-2z" /></svg
      >
      <span>Download</span>
    </button>
  </div>
</div>
