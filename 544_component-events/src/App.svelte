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

  const f_add = () => {
    arr = [...arr, String(arr.length)];
  };


</script>

<main>
  <Button on:add={f_add}></Button>

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