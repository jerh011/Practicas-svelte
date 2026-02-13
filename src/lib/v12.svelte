<script>
 let input;
 let hola;

function focus(){
    console.log(hola)
    if(input){
        input.focus() 
    }
    console.log("buscar cosas hecho click");
 }

</script>
<p bind:this={hola}>hola</p>
<input type="text" placeholder="buscar" bind:this={input}>
<button type="button" on:click={focus}> buscar</button>