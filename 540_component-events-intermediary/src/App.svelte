<!-- https://youtu.be/9Bk7XFRMzgI -->
<script>
  import Component from './Component.svelte';

  const f = () => {
    console.log('f() invoked [Parent]');
  };
</script>

<main>
  <Component f={f} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>