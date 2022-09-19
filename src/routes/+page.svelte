<script>
    let nombre="world"

    let cambiarNombre = () => nombre="nat"
    
</script>

<div  class="flex">
    <h1 on:click={cambiarNombre} class="text-3xl shadow-xl font-bold bg-sky-600 text-white rounded-full px-3 py-2 text-center hover:bg-sky-800 m-4">
        Hello {nombre}!
      </h1>
</div>
