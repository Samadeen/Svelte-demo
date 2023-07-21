<!-- Login.svelte -->

<script>
	let username = '';
	let password = '';

	function handleLogin() {
		console.log('Username:', username);
		console.log('Password:', password);
		window.location.href = '/dashboard';
	}
</script>

<main>
	<h1>Login</h1>
	<form on:submit|preventDefault={handleLogin}>
		<label>
			Username:
			<input type="text" bind:value={username} required />
		</label>
		<label>
			Password:
			<input type="password" bind:value={password} required />
		</label>
		<button type="submit">Login</button>
	</form>
</main>

<style>
	main {
		max-width: 400px;
		margin: 0 auto;
		padding: 20px;
	}

	h1 {
		text-align: center;
	}

	label {
		display: block;
		margin-bottom: 10px;
	}

	input {
		width: 100%;
		padding: 10px;
		margin-bottom: 15px;
	}

	button {
		background-color: #007bff;
		color: #fff;
		border: none;
		padding: 10px 20px;
		cursor: pointer;
	}
</style>
