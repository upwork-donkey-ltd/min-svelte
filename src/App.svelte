<script>
  let value = "Hello"

  $: error = !isValid(value)
  function isValid(v){
    return v.length > 5 && v.length <10
  }
</script>

<h1>Application</h1>
<input type="text" bind:value={value} class:red={error} class:green={!error}/>

{#if value.length < 5}
  <p>Длина меньше 5 символов</p>
{:else if value.length > 10}
  <p>Длина больше 10 символов</p>
{:else}
  <p>Длина между 5 и 10</p>
{/if}

<style>
  input {
    outline: none;
  }
  .red {
    border-color: red;
  }
  .green {
    border-color: green;
  }
</style>
