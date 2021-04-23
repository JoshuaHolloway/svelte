<!-- https://youtu.be/9Bk7XFRMzgI -->
<script>
  import Button from './Button.svelte';
  import LineItem from './LineItem.svelte';

  let arr = ['zero', 'one', 'two', 'three'];

  const f_remove = (e) => {
    arr = arr.filter((elem, idx) => {
      return idx !== e.detail
    });
  };

  const f = (e) => {
    console.log(`Button ${e.detail} in f() invoked [Parent]`);
  };

  const g = (e) => {
    console.log(`Button ${e.detail} in g() invoked [Parent]`);
  };
</script>

<main>
  <Button on:click_1={f} on:click_2={g}></Button>


  {#each arr as elem, idx}
     <LineItem on:remove={f_remove} id={idx} name={elem}/>
     <hr>
  {/each}
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}
</style>