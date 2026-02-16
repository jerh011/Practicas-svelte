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
    let error=null;
    let sectores= ['Backend','Frontend','Devops','QA']
    function envio(e){
        e.preventDefault();//evita que recargue la pagina
        alert(JSON.stringify(estado));
    }
    function actualizarSalario(e){
       estado.salario.min=e.detail.min;
       estado.salario.max=e.detail.max;

       if(estado.salario.min>estado.salario.max){
        error="No puedes tener mas en el minimo que en el maximo"
       }
       else{
        error=null;
       }
    }
</script>
<main>
    <form on:submit={envio}>
      <Input identificador="nombre" label="nombre" bind:value={estado.nombre}/>
      <Input identificador="apelllido" label="apellido" bind:value={estado.apellido}/>
      <Dropdown identificador="sector" label="sector" choices={sectores} bind:value={estado.sector}/>
      <Rangos
        identifier="salario"
        label="salario"
        bind:min={estado.salario.min}
        bind:max={estado.salario.max}
        on:update={actualizarSalario}
        />
        {#if error!=null}
            <p>{error}</p>
        {/if}
      
      <p>
          <input type="submit" value="Enviar" disabled={error!=null}>
      </p>
    </form>
</main>