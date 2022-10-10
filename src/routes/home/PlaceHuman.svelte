<script>
  import Full from "./Full.svelte";
  import Lower from "./Lower.svelte";
  import Upper from "./Upper.svelte";

  export let section;
</script>

<div class="flex grow justify-center">
  {#if section == "Lower section"}
    <Lower />
  {:else if section == "Upper section"}
    <Upper />
  {:else if section == "Full body"}
    <Full />
  {/if}
</div>
