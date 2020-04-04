<script>
  export let name = "Undefied Name"
  export let age = "Undefined Age"
  export let job = "Undefined Job"
</script>

<div>
  <p>Имя: <b>{name}</b></p>
  <p>Вид деятельности: <b>{job}</b></p>

  {#if age < 18}
    <p>Спиртное не продавать!</p>
  {:else}
    <p>Делай что хочешь!</p>
  {/if}
</div>

<style>
  div {
    border: 1px solid black;
    padding: 1rem;
    margin-bottom: 1rem;
  }
</style>
