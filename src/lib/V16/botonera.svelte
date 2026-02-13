<script>
    import Boton from "./boton.svelte";
    import {createEventDispatcher} from "svelte"

    const distpatch  =createEventDispatcher();
    function reinicio(){
        distpatch("reiniciar");
       
    }
 
</script>
<Boton on:pulsado/>
<button type="button" on:click={reinicio}  >Reiniciar</button>