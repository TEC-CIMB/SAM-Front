<script>
  export let name;
  export let date;
  export let test;
  export let age;
  export let weight;
  export let height;
  export let gender;
  export let comments;
</script>

<div class="flex grow bg-[#eaedf0]">
  <div
    class="m-14 grid grow grid-cols-3 gap-6 rounded bg-white shadow-2xl print:m-0 print:shadow-none"
  >
    <div class="flex">
      <img class="m-10 h-14 print:hidden" src="2.png" alt="sam" />
    </div>
    <div class="col-start-3 flex justify-end">
      <img class="m-14 flex h-8 print:hidden" src="CIMB.png" alt="CIMB" />
    </div>
    <div class="col-start-3 mt-10 flex justify-center print:mt-0">
      <div class="font-bold">Date:</div>
      <div>
        {date}
      </div>
    </div>
    <div class="col-start-1 ml-28 flex">
      <div class="font-bold">Name:</div>
      <div>
        {name}
      </div>
    </div>

    <div class="col-start-1 ml-28 flex">
      <div class="font-bold">Test:</div>
      <div>
        {test}
      </div>
    </div>
    <div class="col-start-1 ml-28 flex flex-col">
      <div class="flex font-bold">Age:</div>
      <div>
        {age}
      </div>
    </div>
    <div class="flex flex-col">
      <div class=" font-bold">Gender:</div>
      <div>
        {gender}
      </div>
    </div>
    <div class="col-start-1 ml-28 flex flex-col">
      <div class="font-bold">Weight:</div>
      <div>
        {weight}
      </div>
    </div>
    <div class="flex flex-col">
      <div class="font-bold">Height:</div>
      <div>
        {height}
      </div>
    </div>
    <div class="col-span-3 col-start-1 mt-16 flex-col">
      <div class="mb-10 flex justify-center font-bold">Graphics:</div>
      <div class="flex justify-center"><img src="exp.jpg" alt="" /></div>
    </div>
    <div class="col-span-3 col-start-1 mt-16 flex-col">
      <div class="mb-10 flex justify-center font-bold">Comments:</div>
      <div class="mb-10 flex justify-center">{comments}</div>
    </div>

    <button
      class="col-start-2 m-10 flex items-center justify-center rounded bg-[#022352e0] p-1 font-bold text-white hover:bg-[#02235259] print:hidden"
      on:click={() => window.print()}>Click to print</button
    >
  </div>
</div>
