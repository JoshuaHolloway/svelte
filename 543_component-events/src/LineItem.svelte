<script>
  import {createEventDispatcher} from 'svelte';
  const dispatch = createEventDispatcher();
  export let name;
  export let id;
</script>

<div on:click={() => dispatch('remove', id)}>
  {id}: {name}
</div>

<style>
  div {
    background: darkorange;
  }
</style>