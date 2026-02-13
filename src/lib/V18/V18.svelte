<script>
    import Input from "./lib/input.svelte";
    import Dropdown from "./lib/Dropdown.svelte";
    import Rangos from "./lib/Rangos.svelte";
    let estado={
        nombre: "Pepita",
        apellido: "Flores",
        sector: "Frontend",
        salario:{
            min:25000,
            max:45000
        },
    }
    let sectores= ['Backend','Frontend','Devops','QA']
 function envio(e){
    e.preventDefault();//evita que recargue la pagina
    alert(JSON.stringify(estado));
 }
</script>
<main>
    <form on:submit={envio}>
      <Input identificador="nombre" label="nombre" bind:value={estado.nombre}/>
      <Input identificador="apelllido" label="apellido" bind:value={estado.apellido}/>
      <Dropdown identificador="sector" label="sector" choices={sectores} bind:value={estado.sector}/>
      <Rangos identifier="salario" label="salarios" min={estado.salario.min} max={estado.salario.max}/>
      <p>
          <input type="submit" value="Enviar">
      </p>
    </form>
</main>