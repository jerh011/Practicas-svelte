<script>
    import Input from "./lib/input.svelte";
    let nombre="John",apellido="Doe";

</script>
<main>
      <Input identificador="nombre" label="nombre" bind:value={nombre}/>
      <Input identificador="apelllido" label="apellido" bind:value={apellido}/>
      <p>Tu nombre es {nombre} {apellido}</p>  
</main>


<style>
    :global(body){
        font-family: Arial, Helvetica, sans-serif;
        font-size: 16px;
    }
    :global(*){
        box-sizing: border-box;
    }
</style>