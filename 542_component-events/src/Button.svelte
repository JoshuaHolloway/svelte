<script>
  import {createEventDispatcher} from 'svelte';
  const dispatch = createEventDispatcher();
</script>

<button on:click={() => dispatch('click_1', 1)}>
  Button 1
</button>

<button on:click={() => dispatch('click_2', 2)}>
  Button 2
</button>