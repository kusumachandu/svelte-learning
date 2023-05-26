<script>
	import Form from '../routes/login/+page.svelte';
</script>

<svelte:head>
	<title>Home</title>
	<meta name="description" content="Svelte demo app" />
</svelte:head>

<div>
	<h1>The svelte site</h1>
</div>
<div class="form-div">
	<h1>Login</h1>
	<div id='form'>
		<Form />
	</div>
</div>

<style>

	h1 {
		width: 100%;
		text-align: center;
	}

	#form {
		display: flex;
		flex-direction: column;
		width: 100%;
	}

	.form-div {
		background-color: white;
		width: 50%;
		margin: auto;
		padding: 10px;
		border-radius: 20px;
	}

</style>
