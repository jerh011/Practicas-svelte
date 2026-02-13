<script>
    import Input from "./lib/input.svelte";
    let estado={
        nombre: "Pepita",
        apellido: "Flores",
        sector: "Frontend",
        salario:{
            min:25000,
            max:45000,
        },
    }
 function envio(e){
    e.preventDefault();//evita que recargue la pagina
    alert(JSON.stringify(estado));
 }
</script>
<main>
    <form on:submit={envio}>
      <Input identificador="nombre" label="nombre" bind:value={estado.nombre}/>
      <Input identificador="apelllido" label="apellido" bind:value={estado.apellido}/>
      <Input identificador="nombre" label="nombre" bind:value={estado.nombre}/>
    </form>
</main>