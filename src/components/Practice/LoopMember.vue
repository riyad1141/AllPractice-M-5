<script setup>

const persons = [
  {
    id: 1,
    name: "John Doe",
    Occupation: "Software Engineer",
    Location : "new york",
    Image : "https://images.pexels.com/photos/2182970/pexels-photo-2182970.jpeg?cs=srgb&dl=pexels-linkedin-sales-navigator-2182970.jpg&fm=jpg"
  },
  {
    id: 2,
    name: "Jane smith",
    Occupation: "Software Developer",
    Location : "Los-angles",
    Image : "https://images.pexels.com/photos/2182970/pexels-photo-2182970.jpeg?cs=srgb&dl=pexels-linkedin-sales-navigator-2182970.jpg&fm=jpg"
  },
  {
    id: 3,
    name: "sam Smith",
    Occupation: "Graph Designer",
    Location : "California",
    Image : "https://images.pexels.com/photos/2182970/pexels-photo-2182970.jpeg?cs=srgb&dl=pexels-linkedin-sales-navigator-2182970.jpg&fm=jpg"
  },

];

</script>

<template>

  <section class="grid grid-cols-3 gap-8">
    <div class="bg-white p-6 rounded-md shadow-md text-center" v-for="person in persons" :key="person.id">
      <img :src="person.Image" :alt="person.name" class="md-4 rounded-full mx-auto w-20" :class="person.id === 2? 'h-40':'h-20'">
      <h2 class="text-lg font-bold mb-2">{{person.name}}</h2>
      <p class="text-gray-700">{{person.Occupation}}</p>
      <p class="text-gray-700">{{person.Location}}</p>
    </div>
  </section>


</template>

<style scoped>

</style>