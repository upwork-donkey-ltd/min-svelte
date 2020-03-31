<script>
	let name = 'Svelte';
  let inputValue = "";
  let pos = {
    x: 0,
    y: 0
  }
  function changeNameHandler(){
    name = "This name changed!";
  }
  function mousemoveHandler(event){
    pos.x = event.x;
    pos.y = event.y;
  }
  function submitHandler(event){
    // event.preventDefault();
    console.log("inputvalue: ", inputValue);
  }
</script>

<h1>{name}</h1>
<button on:click={changeNameHandler}>Change name</button>
<div class="playground" on:mousemove={mousemoveHandler}>
  <h2>X: {pos.x}, Y: {pos.y}</h2>
</div>
<form on:submit|preventDefault|once={submitHandler}>
  <input type="text" on:input={event =>(inputValue = event.target.value)} />
  <button type="submit">Submit form</button>
</form>

<style>
	:global(h1) {
		color: purple;
	}
  .playground {
    width: 400px;
    height: 200px;
    padding:1rem;
    margin-bottom: 1rem;
    border: 1px solid black;
  }
</style>
