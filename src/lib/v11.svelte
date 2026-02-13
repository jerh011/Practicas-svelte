<script>
  let nombre = "Luna";

  function escribir(e) {
    nombre = e.target.value;
  }
</script>

<p>Tu nombre es {nombre}</p>

<!-- <input
  type="text"
  value={nombre}
  on:keyup={escribir}a
/> -->
<input type="text"
bind:value={nombre}>