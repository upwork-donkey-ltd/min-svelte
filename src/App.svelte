<script>
  import Person from './Person.svelte';
  const people = [
    {id: 1, name: "Goddess", age: 100, job: "Seniorita"},
    {id: 2, name: "Asshole", age: 15, job: "Conjier"}
  ]

  let name="Barmaley"
  let age = 20
  let jobTitle = "ZombiKiller"
</script>

<h1>Application</h1>

<Person name={people[0].name} age={people[0].age} job={people[0].job} />
<Person {...people[1]} />
<Person {name} {age} job={jobTitle} />

<style>
</style>
