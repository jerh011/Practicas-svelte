<script>
    function fetch(){
        return new Promise ((resolver,reject)=>{
             setTimeout(()=>{resolver({
            //     nombre:"Rita la Cantadora",
            //     edad:41,
            //     ocupacion:"cantadora"
             })
            reject("tenbenis yb oribklema para sacar los datos")
        },3000);
    })
    
    }
  
</script>
{#await fetch()}
    <p>un segundo que estamos resolviendo cosas...</p>
{:then  payload} 
    <p>Nombre:{payload.nombre}</p>
    <p>Edad:{payload.edad}</p>
    <p>Ocupacion:{payload.ocupacion}</p>
{:catch e}
<strong>ERROR:{e} </strong>
{/await}