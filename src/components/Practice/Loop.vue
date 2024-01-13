<script setup>

const numbers = [1, 2, 3, 4, 5, 6, 7];
const tasks = [
    "Complete Project Proposal",
    "update website content",
    "fix bug in user authentication",
    "prepare preparation for project",
    "Test new feature implementation"
]

</script>

<template>

  <section class="flex space-x-4">
    <div class="number-box" v-for="(number, index) in numbers" :key="index">
      {{number}}
    </div>
    <div v-for="(task, index) in tasks" :key="index">
      {{task}}
    </div>
  </section>

</template>

<style scoped>

.number-box{
  background-color: #3490dc;
  color: #ffffff;
  font-weight: bold;
  padding: 10px;
  border-radius: 8px;
}

</style>