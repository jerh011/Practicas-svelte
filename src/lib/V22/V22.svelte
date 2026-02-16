<script>
    export let choices = ["red", "yellow", "blue", "green"];
    export let color = choices[0];

    let backgrounds = {
        red: 'silver',
        yellow: 'silver',
        blue: 'yellow',
        green: 'purple'
    };
</script>
<!-- <p style={`color: ${value};`} class="color">{value}</p> -->
<!-- <p style:color={value} class="color">{value}</p> -->
<!-- <p style:color class="color">{color}</p> -->
<!-- <div class="divcentrado">
    <p style:color={color} style:background-color={backgrounds[color]}
    class="color"> -->
<p
    style:--bgcolor={backgrounds[color]}
    style:--fgcolor={color}
    class="color"
>
    {color}
</p>

<select bind:value={color}>
    {#each choices as choice}
    <option value={choice}>{choice}</option>
    {/each}
</select>


<style>
    .color{
        background-color: var(--bgcolor);
        color: var(--fgcolor);

        font-size: 40px;
        margin: 0;
        line-height: 1;
        font-weight: bold;
        padding: 10px;
    }

   
</style>