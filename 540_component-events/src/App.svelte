<!-- https://youtu.be/9Bk7XFRMzgI -->
<script>
  import Button from './Button.svelte';

  const f = () => {
    console.log('f() invoked [Parent]');
  };
</script>

<main>
  <Button on:click={f}></Button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>