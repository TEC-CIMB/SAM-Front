<script>
  import DataInput from "./DataInput.svelte";
  import Section from "./Section.svelte";
  let step = "input";
  let files;
  let name;
  let date;
  let test;
  let age;
  let weight;
  let height;
  let gender;
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
