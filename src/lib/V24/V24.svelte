<script>
    import "../../assets/globa.css"
    import Input from "./lib/input.svelte";
    let nombre="John",apellido="Doe";

</script>
<main>
      <Input label="nombre" bind:value={nombre}/>
      <Input label="apellido" bind:value={apellido}/>
      <p>Tu nombre es {nombre} {apellido}</p>  
</main>


<style>
   :global(body){
     font-family: Impact, Haettenschweiler, 'Arial Narrow Bold', sans-serif;
   }
</style>