<script>
	let name = 'Svelte';
  let counter = 0;
  $: counterClass = counter % 2===0 ?"red":"blue";
  $: upperName = name.toUpperCase();
  $: lowerName = name.toLowerCase();
  $: {
    console.log("Name: ", name);
    console.log("Counter: ", counter);
  }
  $: if (counter === 10){
    name = "Counter is equal 10"
  }
  function changeName(){
    name = "New name";
  }
</script>

<h1>{name}</h1>
<h2>{upperName}</h2>
<h2>{lowerName}</h2>
<button on:click={changeName}>Change name</button>

<h2 class={counterClass} >Counter {counter}</h2>
<button on:click={()=>counter++}>Add 1 to counter</button>

<style>
 .blue{
  color: blue;
 }
 .red{
  color: red;
 }
</style>
