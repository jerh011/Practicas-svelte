<script>
    import Boton from "./boton.svelte";
    let veces=0;
    let fechas=[];
    function sePulso(event){
        const fecha=event.detail.fecha;
        fechas=[...fechas,fecha];
        veces++;
    }
</script>

<p> Me han pulsado {veces} 
    {veces=== 1? 'vez':'veces'}</p>
<Boton on:pulsado={sePulso}/>
{#each fechas as fech }
    <p>{fech}</p>
{/each}