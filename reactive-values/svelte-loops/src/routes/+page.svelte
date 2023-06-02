<script>
  import "../app.css";

  let peoples = [
    { name: "chandu", age: 23, beltColor: "gray", id: 1 },
    { name: "shekar", age: 23, beltColor: "red", id: 2 },
    { name: "killer", age: 17, beltColor: "pink", id: 3 },
    { name: "monster", age: 18, beltColor: "orange", id: 4 },
  ];
</script>

<header class="font-bold text-center text-2xl">Loops</header>
<main class="py-20">
  <div class="w-1/2 py-10 grid grid-cols-2 gap-3 m-auto items-center justify-center">
    {#each peoples as people}
      <section class="border px-5 py-5 justify-center rounded-lg shadow-lg shadow-pink-200">
        <div>
          <p>{people.name}</p>
          <p style="color: {people.beltColor}">{people.beltColor}</p>
        </div>
        <div>

        </div>
      </section>
    {/each}
  </div>
</main>
