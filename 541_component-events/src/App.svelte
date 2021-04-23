<!-- https://youtu.be/9Bk7XFRMzgI -->
<script>
  import Button from './Button.svelte';

  const f = () => {
    console.log('Button 1 in f() invoked [Parent]');
  };

  const g = () => {
    console.log('Button 2 in g() invoked [Parent]');
  };
</script>

<main>
  <Button on:click_1={f} on:click_2={g}></Button>
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>