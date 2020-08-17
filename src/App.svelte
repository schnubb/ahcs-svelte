<script>
	import Button from "./components/Button.svelte";
	export let name;

	const data = {
		username: "",
		email: ""
	}

	const submitData = () => {
		// implement submit api later
		console.table(data);
	}
</script>

<main>
	<h1>Hello {name}!</h1>
	<p>Visit the <a href="https://svelte.dev/tutorial">Svelte tutorial</a> to learn how to build Svelte apps.</p>
	<form action="" on:submit|preventDefault={submitData}>
		<fieldset>
			<label for="username">Name:</label>
			<input type="text" bind:value={data.username} id="username" />
			<label for="email">E-Mail</label>
			<input type="email" bind:value={data.email} id="email">
			<Button type="submit">
				<span slot="label">Submit</span>
			</Button>
		</fieldset>
	</form>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>