<script>
    import Seccion from "./lib/Seccion.svelte";

    function no(){
        alert("no se puede copiar");
    }
</script>

<svelte:body on:keyup={no} />

<Seccion titulo="Menú del dia">

    <svelte:fragment slot="main">
        <p>nachos</p>
    </svelte:fragment>

    <h1 slot="header">aa</h1>

</Seccion>
