<script>
	let name = 'Irene';
  let color = 'black';
  const handleClick = () => {
    color = 'orange';
  };
  const handleInput = (e) => {
    color = e.target.value;
  };
</script>

<main>
	<h1>{name}</h1>
	<p style="color: {color}">{color} belt</p>
  <button on:click={handleClick}>update belt colour</button>
  <!-- <input type="text" on:input={handleInput} value={color}> -->
  <input type="text" bind:value={color}>
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