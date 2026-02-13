<script>
    let acepta= false;
</script>

{#if  acepta}
    <p>Nos hanb dicho que si</p>
{:else}
<p>nos dice que no </p>
    
{/if}
<p>
    <label >
        <input type="checkbox" bind:checked={acepta}>
        Modificar mi valor
    </label>
</p>