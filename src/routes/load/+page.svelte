<script>
  let nombre = "world";

  let cambiarNombre = () => (nombre = "Dr. Rogelio y Claudia");
</script>

<div class="h-full w-full bg-[#ebf2fe]">
  <h1
    on:click={cambiarNombre}
    class="m-4 rounded-full bg-sky-600 px-3 py-2 text-center text-3xl font-bold text-white shadow-xl hover:bg-sky-800"
  >
    Cargar {nombre}!
  </h1>
</div>
