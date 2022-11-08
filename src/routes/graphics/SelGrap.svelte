<script>
  import DataVisualization from "./DataVisualization.svelte";

  export let selection;

  export let Kcheck;
  export let Hcheck;
  export let Acheck;

  export let UPcheck;
  export let FBcheck;
  export let RLcheck;
</script>

{#if selection !== null}
  {#if selection == "Angles"}
    <DataVisualization
      {Kcheck}
      {Hcheck}
      {Acheck}
      {UPcheck}
      {FBcheck}
      {RLcheck}
    />
  {:else if selection == "Angular Velocity"}
    <div>Building</div>
  {/if}
{/if}
