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
<p>tu nombre tiene {nombre.length} carateres</p>
<style>
    .texto{
        font-size: 1.6rem;
    }
</style>