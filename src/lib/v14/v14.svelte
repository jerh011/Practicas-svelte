<script>
    import Boton from "./boton.svelte";
    let veces=0;
    function sePulso(){
        veces++;
    }
</script>

<p> Me han pulsado {veces} 
    {veces=== 1? 'vez':'veces'}</p>
<Boton on:pulsado={sePulso}/>