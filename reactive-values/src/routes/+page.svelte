<script>
  import '../app.css';
  let firstName = 'chandu';
  let lastName = 'kusuma';
  let color = 'black';

  $: fullName = `${firstName} ${lastName}`;

</script>

<main class="pt-10">
  <h1 class="font-bold text-center text-2xl">Reactive Values</h1>
</main>
<div class="text-center pt-20">
  <p><span class="px-2">{fullName}:</span><span>Belt-</span><span style="color: {color}">{color}</span></p>
</div>
<section class="py-10"></section>
<section class="w-1/2 flex m-auto px-5 py-10">
  <div class="">
    <label>First Name</label>
    <input type="text" placeholder="Enter first name" bind:value={firstName} class="border px-1 py-1 rounded-lg" />
  </div>
  <div class="">
    <label>Last Name</label>
    <input type="text" placeholder="Enter last name" bind:value={lastName} class="border px-1 py-1 rounded-lg" />
  </div>
  <div class="">
    <label>Belt Color</label>
    <input type="text" placeholder="enter the color" bind:value={color} class="border px-1 py-1 rounded-lg" />
  </div>
</section>
