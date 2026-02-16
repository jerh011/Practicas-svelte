<script>
    import { preventDefault } from "svelte/legacy";

    let contador=1;
    let disabled=false;
    let valor="Svelte";
    function desactivar (e){
        disabled=true;
    }
    const inc=()=> contador=contador+1;
    const des=()=> contador=contador-1;
</script>
<main>
    <form action="/search" method="post" on:submit|preventDefault={desactivar}>
    <p>
        <input type="text" bind:value={valor}  disabled={disabled}/>
        <button type="submit" value="Buscar" disabled={disabled}>Buscar</button>
    </p>
    </form>
    <h1>
        <button type="button" on:click={des}>-</button>
        {contador}
        <button type="button" on:click={inc}>+</button>
    </h1>
</main>