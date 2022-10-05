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
    <Graphics bind:comments />
  {:else if screen == "save"}
    <Save {name} {date} {test} {age} {weight} {height} {gender} {comments} />
  {:else if screen == "help"}
    <Help />
  {/if}
</Layout>
