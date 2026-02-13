<script>
    import {createEventDispatcher} from "svelte";
    
    export let identifier;
    export let label;

    export let min;
    export let max;
    
    const dispatch=createEventDispatcher();

</script>
<p>
    <label id={identifier + "_min"}>{label} minimo</label>
    <input type="range" min={0} max={5000} value={min}/>
</p>

<p>
    <label id={identifier + "_max"}>{label} maximo</label>
    <input type="range" min={0} max={5000} value={max}/>

</p>

