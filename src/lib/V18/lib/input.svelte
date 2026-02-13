<script>
    export let identificador
    export let value
    export let label
</script>

  <p>
            <label for={identificador}>{label}</label>
            <input id={identificador} type="text" bind:value>
  </p>