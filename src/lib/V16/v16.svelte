<script>
    import Botonera from "./botonera.svelte";
    let veces=0;
    
    function sePulso(){
        console.log("xd");
        veces++;
    }
    function volverAcero(){
        veces=0;
    }
</script>

<p> Me han pulsado {veces} 
    {veces=== 1? 'vez':'veces'}</p>
<Botonera on:reiniciar={volverAcero} on:pulsado={sePulso}/>
