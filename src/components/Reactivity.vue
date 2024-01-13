<script setup>
import {ref} from "vue";

const tasks = ref([
  {
    id: 1,
    name: "Task 1"
  },
  {
    id: 2,
    name: "Task 2"
  },
  {
    id: 3,
    name: "Task 3"
  }
]);

function addNewTask() {
  const newTask = {
    id: tasks.value.length+1,
    name: `Task ${tasks.value.length+1}`
  };
  tasks.value.push(newTask);
}



// function addNewTask() {
//   const id = prompt("Enter your id");
//   const name = prompt("Enter your name");
//   const newTask = {
//     id: id,
//     name: name
//   };
//   tasks.value.push(newTask);
// }

</script>

<template>

  <div>
    <h1>Tasks</h1>
    <ul>
      <li v-for="task in tasks" :key="task.id">
        {{task.name}}
      </li>
    </ul>
    <button @click="addNewTask()">Add new Task</button>
  </div>


</template>

<style scoped>

</style>