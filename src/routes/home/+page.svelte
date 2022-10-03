<script>
  import DataInput from "./DataInput.svelte";
  import Section from "./Section.svelte";
  let step = "input";
  export let files;
  export let name;
  export let date;
  export let test;
  export let age;
  export let weight;
  export let height;
  export let gender;
</script>

{#if step == "input"}
  <DataInput
    bind:step
    bind:files
    bind:name
    bind:date
    bind:test
    bind:age
    bind:weight
    bind:height
    bind:gender
  />
{:else if step == "section"}
  <Section {files} />
{/if}
