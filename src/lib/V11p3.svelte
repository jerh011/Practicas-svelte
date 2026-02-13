<script>
    let valores=["africa","america","asia","europa","oseania"]
let valor="asia";
</script>
<select bind:value={valor}>
    {#each valores as v }
        <option value="{v}">{v}</option>
    {/each}
</select>
<p>Has decidido {valor}</p>