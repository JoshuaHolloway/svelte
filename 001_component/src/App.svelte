<script>
  import Nested from './Nested.svelte';
	export let name;
</script>

<main>
	<h1>Hello {name}!</h1>
	<p class="test">Inside App.svelte!</p>

  <Nested x=5/>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}


  p {
    background: darkorchid;
  }

  .test {
    color: deeppink;
  }
</style>