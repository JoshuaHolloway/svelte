<script>
  import DeleteButton from './DeleteButton.svelte';

  export let name;
  export let id;
  export let f;
</script>

<div>
  <span>{id}: {name}</span>
  <DeleteButton on:remove={f} id={id}/>
</div>

<style>
  div {
    background: deepskyblue;
    padding: 10px;
  }
</style>