<script>
    export let value = "";
    export let label = "";

    $: id = "_" + label.toLowerCase();
    let invalid=value.length===0;
    let valid=value.length>0;
    function actualice(){
      invalid=value.length===0;
      valid=value.length>0;
    }
</script>

<!-- <p class={value.length > 0 ? "valid" : "invalid"}> -->
<!-- <p class:invalid={value.length===0}> -->
<p class:invalid class:valid> 
  <label for={id} class="label">{label}</label>
  <input id={id} type="text" bind:value={value} on:keyup={actualice}>
</p>

<style>
.label { color: blue; }
input {
    width: 100%;
    border: 1px solid gray;
    border-radius: 2px;
    padding: 5px;
}
.valid input{
  background-color: #c0f0c0;
}
.invalid input{
  background-color: #f8c0c0;
}
</style>

