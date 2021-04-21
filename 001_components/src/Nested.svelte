<script>
  export let x = 0;
  
  // Prop available immediately:
  console.log(`x in Nested.svelte: ${x}`);

  // -const, class, and functions are read-only
  //  outside the component
  export const k = -1;
  export class Class {}
  export function func() {
    return 0;
  }

  // Function expression as prop
  export const f = n => n.toFixed(2);

  const str = 'contains <strong>code!</strong> via HTML';
</script>

<p class="test">From Nested.svelte!</p>

<p>{@html str}</p>

<p>x: {x}</p>
<p>f: {f}</p>

<style>
  p {
    background: deepskyblue;
  }
</style>