<script>
  import {addTodo} from '../stores/todoStore';
  import TodoCard from './TodoCard.svelte';
  let todo = "";

  function handleSubmit() {
    addTodo(todo);

    todo = '';
  }

</script>

<main class="">
  <form on:submit|preventDefault={handleSubmit}>
    <label class="flex border items-center rounded-lg bg-blue-300">
      <p class='px-2'>Todo</p>
      <input 
        type="text"
        bind:value={todo}
        placeholder="Enter the Todo"
        class='py-2 px-2 focus:outline-none border rounded-r-lg'
      />
    </label>
    <div class="py-5 text-center">
      <button class="uppercase border px-5 rounded-lg py-1 bg-gradient-to-tr from-slate-400 to-slate-100">Create</button>
    </div>
  </form>
</main>
<div class="w-3/4">
  <TodoCard />
</div>