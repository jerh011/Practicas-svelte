<script>
    import {createEventDispatcher} from "svelte"
    let dispatch= createEventDispatcher();
    function pulsar(){
        dispatch("pulsado");
    }
</script>

<button type="button" 
        on:click={pulsar}>
    Tu púlsame
</button>