<script>
	import Header from './Header.svelte';
</script>

<div class="app">
	<Header />
	<main>
		<slot />
	</main>
</div>

<style>
	.app {
		background-color: rgb(201, 201, 201);
		height: 100vb;
	}
</style>
