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
        <img src="K_FE.jpeg" alt="KFE" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="K_R.jpeg" alt="KR" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="K_AA.jpeg" alt="KAA" />
      </div>
    {/if}
  {/if}
  {#if Hcheck}
    {#if UPcheck}
      <div class="w-full">
        <img src="H_FE.jpeg" alt="HFE" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="H_R.jpeg" alt="HR" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="H_AA.jpeg" alt="HAA" />
      </div>
    {/if}
  {/if}

  {#if Acheck}
    {#if UPcheck}
      <div class="w-full">
        <img src="A_FE.jpeg" alt="AFE" />
      </div>
    {/if}
    {#if FBcheck}
      <div class="w-full">
        <img src="A_R.jpeg" alt="AR" />
      </div>
    {/if}
    {#if RLcheck}
      <div class="w-full">
        <img src="A_AA.jpeg" alt="AAA" />
      </div>
    {/if}
  {/if}
</div>
