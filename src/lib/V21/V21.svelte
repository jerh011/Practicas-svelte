<script>
    import Input from "./lib/input.svelte";
    let nombre="John"
    let apellido="Doe"
</script>
<fieldset>
    <Input bind:value={nombre} label="Nombre" />
    <Input bind:value={apellido} label="Apellido" />
</fieldset>
<p class="label"> 
    tu eres <strong>{nombre} {apellido}</strong>
</p>
<style>
    .label{
        color: darkblue;
        font-size: 1.3rem;
       text-decoration: underline;
    }
</style>