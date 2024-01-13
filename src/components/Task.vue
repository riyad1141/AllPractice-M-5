<script setup>
import {ref} from "vue";

const tasks = ref([
  { id: 1, name: 'Task 1', minutes: 30 },
  { id: 2, name: 'Task 2', minutes: 15 },
  { id: 3, name: 'Task 3', minutes: 45 }
]);

function removeTask(index) {
  tasks.value.splice(index, 1);
}

</script>

<template>

    <div class="container mx-auto p-4">
      <h1 class="text-2xl font-bold mb-4">Tasks</h1>
      <ul class="list-disc list-inside">
        <li v-for="(task, index) in tasks" :key="task.id" class="py-2">
          <div class="flex items-center justify-between">
            <span class="text-gray-700">{{ task.name }} ({{ task.minutes }} minutes)</span>
            <button @click="removeTask(index)" class="bg-red-500 hover:bg-red-700 text-white font-bold py-1 px-2 rounded">
              Remove
            </button>
          </div>
        </li>
      </ul>
    </div>
  </template>

<style scoped>

</style>