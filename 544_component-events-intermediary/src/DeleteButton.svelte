<script>
  import {createEventDispatcher} from 'svelte';
  const dispatch = createEventDispatcher();
  export let id;
</script>

<div on:click={() => dispatch('remove', id)}>
  Delete Button
</div>

<style>
  div {
    background: darkorange;
  }
</style>