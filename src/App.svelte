<script>
	let name = 'july';
	function handleClick(){
		name = 'otro nombre'
	}
</script>

<main>
	<h1>Bienvenido a  Italia 🦮</h1>
	<button on:click={handleClick}>En construccion</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff0080;
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