<script>
    import {createEventDispatcher} from "svelte"
    let dispatch= createEventDispatcher();
    function pulsar(){
        let timestamp=new Date();
        let ahora= timestamp.toLocaleString();
        dispatch("pulsado",{ fecha:ahora});
    }
    
</script>

<button type="button" 
        on:click={pulsar}>
    Tu púlsame
</button>
