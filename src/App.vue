<script setup>
import HelloWorld from './components/HelloWorld.vue'
import HelloWorld2 from './components/HelloWorld2.vue'
import { ref } from "vue";

let database = ref([
  {
    name: "Johnny",
    department: "Marketing",
    salary: 30000
  },
  {
    name: "Todd",
    department: "Worker",
    salary: 5000
  },
  {
    name: "Micheal",
    department: "Dancer",
    salary: 90000
  },
  {
    name: "John",
    department: "Contractor",
    salary: 48500
  },
  {
    name: "Peter",
    department: "Athlete",
    salary: 111500
  },
])

const deleteCard = (position) => database.value.splice(position, 1)
</script>

<template>
  <main>
    <!-- <HelloWorld
      :name="database[0].name"
      :department="database[0].department"
      :salary="database[0].salary"
      :position="0"
    /> -->

    <HelloWorld2
      @destroy="deleteCard"
      v-for="(item, index) in database"
      :name="item.name"
      :department="item.department"
      :salary="item.salary"
      :position="index"
      />
  </main>
</template>

<style scoped>
main {
  /* align-items: center; */
  display: flex; 
  /* flex-direction: column; */
  flex-wrap: wrap;
}

.container {
border: 1px solid rgb(124, 191, 202);
width: 300px;
/* margin: 1em auto 1em auto; */
margin-right: 30px;
margin-bottom: 30px;
padding: 1em;
border-radius: 5px;
font-size: 1.3em;
}



</style>
