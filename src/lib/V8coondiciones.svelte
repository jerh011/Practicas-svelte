<script>
    let nombre="";
    function Handle(e){
        //  e de evento 
        const target= e.target;
        nombre=e.target.value;
        console.log(nombre)
    }
    
</script>
<br><br>
<input type="text" placeholder="pon tu nombre" class="texto" on:keyup={Handle}/>
<!-- <button disabled={nombre.length===0}>enviar mensaje</button> -->
<p>tu nombre tiene {nombre.length} carateres</p>
{#if  nombre.length===0}
<p>n me has dicho comoo te llamas</p>
{:else}
<strong>hola, {nombre}</strong>
{/if}
<style>
    .texto{
        font-size: 1.6rem;
    }
</style>