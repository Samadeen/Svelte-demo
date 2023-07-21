<!-- Dashboard.svelte -->

<script>
	// Sample random data for the table
	const data = [
		{ id: 1, name: 'John Doe', age: 30, email: 'john.doe@example.com' },
		{ id: 2, name: 'Jane Smith', age: 28, email: 'jane.smith@example.com' },
		{ id: 3, name: 'Bob Johnson', age: 35, email: 'bob.johnson@example.com' }
		// Add more data as needed
	];
</script>

<main>
	<h1>Welcome to the Dashboard!</h1>
	<table>
		<thead>
			<tr>
				<th>ID</th>
				<th>Name</th>
				<th>Age</th>
				<th>Email</th>
			</tr>
		</thead>
		<tbody>
			{#each data as item}
				<tr key={item.id}>
					<td>{item.id}</td>
					<td>{item.name}</td>
					<td>{item.age}</td>
					<td>{item.email}</td>
				</tr>
			{/each}
		</tbody>
	</table>
</main>

<style>
	main {
		max-width: 800px;
		margin: 0 auto;
		padding: 20px;
	}

	h1 {
		text-align: center;
	}

	table {
		width: 100%;
		border-collapse: collapse;
		margin-top: 20px;
	}

	th,
	td {
		padding: 10px;
		text-align: left;
		border-bottom: 1px solid #ccc;
	}

	th {
		background-color: #f2f2f2;
	}
</style>
