<script>
    import Seccion from "./lib/Seccion.svelte";
</script>



<Seccion titulo="Menú del dia">
    <!-- coon divicion -->
    <!-- <div slot="main">
        <p>nachos</p>
        <p>nachos</p>
        <p>nachos</p>
        <p>nachos</p>
        <p>nachos</p>
        </div> -->
    <!-- sin divicion -->
    <svelte:fragment slot="main">
      <p>nachos</p>
      <p>nachos</p>
      <p>nachos</p>
    </svelte:fragment>
    <h1 slot="header">aa</h1>
</Seccion>

