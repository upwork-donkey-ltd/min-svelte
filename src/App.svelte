<script>
  import Person from './Person.svelte';

  let value = "";
  let people = [
    {id: 1, name: "Goddess"},
    {id: 2, name: "Asshole"},
    {id: 3, name: "Barmaley"}
  ];

  function removeFirst(){
    people = people.slice(1);
  }

  function addPerson(){
    // people = people.concat([
    //  {
    //    id: Date.now(),
    //    name: value
    //  }
    //]);
    people = [...people, {
      id: Date.now(),
      name: value
    }]
    value = "";
  }
</script>

<input type="text" bind:value />
<button on:click={addPerson}>Add Person</button>
<button on:click={removeFirst}>Remove First</button>

<hr>

{#each people as {name, id}, i (id)}
  <Person {name} index={i}/>
{:else}
  <p>No people</p>
{/each}

<style>
</style>
