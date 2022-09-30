<script>
  import DataInput from "./DataInput.svelte";
  import Section from "./Section.svelte";
  let step = "input";
  let files;
</script>

{#if step == "input"}
  <DataInput bind:step bind:files />
{:else if step == "section"}
  <Section {files} />
{/if}
