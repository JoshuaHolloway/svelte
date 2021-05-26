<script>
	export let name;

  // -To change component state and trigger a re-render,
  //  just assign to a locally declared variable
  let count = 0;

  function handleClick() {
    count = count + 1;
  }
</script>

<main>
	<h1>Hello {name} {count}</h1>

  <button on:click={handleClick}>++</button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>