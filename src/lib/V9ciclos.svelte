<script>
    import V9Ejercici from "./V9Ejercici.svelte";
    let elementos=[
        {id:"123123141",nombre:"comprar patatas",terminado:false},
        {id:"51260",nombre:"limpiar el jardin",terminado:true},
        {id:"561596105",nombre:"Enviar correoo",terminado:true},
        {id:"8419856109",nombre:"Llamar a lucia",terminado:false}
]
</script>
{#each elementos as e, num (e.id) }
    <V9Ejercici nombre={e.nombre} terminado={e.terminado}/>
    {:else}
    <p>no hay tareas para hoy</p>
{/each}