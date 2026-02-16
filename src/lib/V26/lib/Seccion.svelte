<script>
  export let titulo;
</script>
<section>
  <h1>{titulo}</h1>
    <slot>
      <p>Pregunta</p>
    </slot>
</section>