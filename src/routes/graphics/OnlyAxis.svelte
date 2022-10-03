<script>
  export let UPcheck = false;
  export let FBcheck = false;
  export let RLcheck = false;
</script>

<h3 class="mb-2 text-lg font-bold">Axis</h3>
<ul
  class="w-full rounded-lg border border-gray-200 bg-white text-sm font-medium text-gray-900"
>
  {#if UPcheck}
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={UPcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Up-Down
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Right-Left
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Front-Back
        </label>
      </div>
    </li>
  {:else if RLcheck}
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Up-Down
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={RLcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Right-Left
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Front-Back
        </label>
      </div>
    </li>
  {:else if FBcheck}
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Up-Down
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          disabled
          id="vue-checkbox"
          type="checkbox"
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Right-Left
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={FBcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Front-Back
        </label>
      </div>
    </li>
  {:else}
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={UPcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Up-Down
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={RLcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Right-Left
        </label>
      </div>
    </li>
    <li class="w-full rounded-t-lg border-b border-gray-200">
      <div class="flex items-center pl-3">
        <input
          id="vue-checkbox"
          type="checkbox"
          bind:checked={FBcheck}
          class="h-4 w-4 rounded border-gray-300 bg-gray-100 text-blue-600 focus:ring-2 focus:ring-blue-500"
        />
        <label
          for="vue-checkbox"
          class="ml-2 w-full py-3 text-sm font-medium text-gray-900"
          >Front-Back
        </label>
      </div>
    </li>
  {/if}
</ul>
