<script>
	import TodoFrom from '../components/TodoFrom.svelte';
	import './app.css';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<section class="border border-gray-200 shadow-lg shadow-blue-200">
	<TodoFrom />
</section>

<style>
	section {
		display: flex;
		flex-direction: column;
		align-items: center;
		flex: 0.6;
		border-radius: 30px;
		padding-top: 40px;
	}
</style>
