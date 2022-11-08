<script>
  import Graphics from "./graphics/Graphics.svelte";
  import Help from "./help/Help.svelte";
  import Home from "./home/Home.svelte";
  import Layout from "./Layout.svelte";
  import Save from "./save/Save.svelte";

  let screen = "initial";
  let name;
  let date;
  let test;
  let age;
  let weight;
  let height;
  let gender;
  let comments;

  export let Kcheck;
  export let Hcheck;
  export let Acheck;

  export let UPcheck;
  export let FBcheck;
  export let RLcheck;
</script>

<Layout bind:screen>
  {#if screen == "initial"}
    <div class="flex grow items-center justify-center bg-[#eaedf0]">
      <img class="w-1/3 " src="sam1.png" alt="sam inicial" />
    </div>
  {:else if screen == "home"}
    <Home
      bind:screen
      bind:name
      bind:date
      bind:test
      bind:age
      bind:weight
      bind:height
      bind:gender
    />
  {:else if screen == "graphics"}
    <Graphics
      bind:comments
      bind:Kcheck
      bind:Hcheck
      bind:Acheck
      bind:UPcheck
      bind:FBcheck
      bind:RLcheck
    />
  {:else if screen == "save"}
    <Save
      {name}
      {date}
      {test}
      {age}
      {weight}
      {height}
      {gender}
      {comments}
      {Kcheck}
      {Hcheck}
      {Acheck}
      {UPcheck}
      {FBcheck}
      {RLcheck}
    />
  {:else if screen == "help"}
    <Help />
  {/if}
</Layout>
