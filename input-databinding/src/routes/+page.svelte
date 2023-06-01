<script>
  import { updated } from '$app/stores';
  import { get } from 'svelte/store';
	import './styles.css';
	let name = '';
	let color = 'red';

	function changeName() {
		name = 'chandu'
	}

	function clickHandler(){
		color = 'orange'
	}
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class=' w-1/2 m-auto'>
	<div class='text-center flex flex-col items-center'>
		<label class="border flex items-center rounded-lg w-1/2">
			<p class='px-3'>color</p>
			<input type="text" id='inputValue' placeholder="enter the color" bind:value={color} class="border py-2 rounded-r-lg px-4 w-full" />
		</label>
		<label class="border flex items-center rounded-lg w-1/2 my-5">
			<p class='px-3'>Name</p>
			<input type="text" id='inputValue' placeholder="enter your name" bind:value={name} class="border py-2 rounded-r-lg px-4 w-full" />
		</label>
		<p class="pt-10 pb-5">
			<span class="px-1">My name is</span><span id='nameText' style="color: {color}" class="font-bold">{name}</span>
		</p>
	</div>
	<div class="text-center">
		the color you entered is {color}	
	</div>
	<div class="flex items-start justify-center py-5">
		<button on:click={clickHandler} class='border px-5 py-1 rounded-lg'>update the color</button>
	</div>
	<div class="flex items-start justify-center">
		<button on:click={changeName} class='border px-5 py-1 rounded-lg'>update the name</button>
	</div>
</section>

<style>
	
</style>
