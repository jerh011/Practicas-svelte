<script>
  
    export let value
    export let label
    let id="_"+label.toLoweCase();
</script>

  <p>
   <label for={id}>{label}</label>
   <input id={id} type="text" bind:value>
  </p>

  <style>
    /* :global(label){
        color:blue;
       font-weight: bold;
    } */
  </style>