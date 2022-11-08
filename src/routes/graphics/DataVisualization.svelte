<script>
  export let Kcheck;
  export let Hcheck;
  export let Acheck;

  export let UPcheck;
  export let FBcheck;
  export let RLcheck;
</script>

<div class="m-10 flex grow flex-col items-center justify-center gap-4">
  {#if Kcheck}
    {#if UPcheck}
      <div class="w-full">
        <img src="AnglesD1_IClau_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="AnglesD2_IClau_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="AnglesD1_IJose_SNat.png" alt="knee" />
      </div>
    {/if}
  {/if}
  {#if Hcheck}
    {#if UPcheck}
      <div class="w-full">
        <img src="AnglesD2_IJose_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="AnglesD2_IClau_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="AnglesD1_IJose_SNat.png" alt="knee" />
      </div>
    {/if}
  {/if}

  {#if Acheck}
    {#if UPcheck}
      <div class="w-full">
        <img src="AnglesD1_IClau_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="AnglesD2_IClau_SNat.png" alt="knee" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="AnglesD1_IJose_SNat.png" alt="knee" />
      </div>
    {/if}
  {/if}
</div>
