<script setup>

const tasks = [
  {
    id: 1,
    title: "Complete Project Proposal",
    status: "In progress",
  },
  {
    id: 2,
    title: "update website content",
    status: "Pending",
  },
  {
    id: 3,
    title: "fix bug in user authentication",
    status: "Done",
  },
  {
    id: 4,
    title: "prepare preparation for project",
    status: "Process",
  },
];

function getCompletedTask() {
  return tasks.filter(task => "In progress" === task.status);
}

</script>

<template>

  <section class="flex" >
    <div class="max-w-md mx-auto bg-white p-8 rounded-md shadow-md">
      <div v-for="task in getCompletedTask()" :key="task.id" class="text-lg font-bold mb-4 bg-red-400" >
        {{task.id}}. {{task.title}}
      </div>
    </div>
  </section>

</template>

<style scoped>

</style>