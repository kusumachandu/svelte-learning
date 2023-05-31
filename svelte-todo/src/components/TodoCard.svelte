<script>
  import {todos} from '../stores/todoStore';
  import {deleteTodo} from '../stores/todoStore';

  function handleDelete(id){
    deleteTodo(id);
    console.log('deleted item successfully');
  }

</script>

<main class="flex flex-col gap-5 w-1/2 m-auto">
  {#each $todos as todo (todo.id)}
    <div class="border min-h-[50px] rounded-lg shadow-lg flex justify-between px-5">
      <li class='list-none px-4 py-5'>
        <p class=''>{todo.text}</p>
      </li>
      <button on:click={() => {handleDelete(todo.id)}} class="text-red-300">delete</button>
    </div>
  {/each}
</main>