<script setup>

const icons = [
  {title: "Sunny", icon: "https://upload.wikimedia.org/wikipedia/commons/thumb/0/08/Weather_icon_-_sunny.svg/512px-Weather_icon_-_sunny.svg.png"},
  {title: "Cloudy", icon: "https://cdn-icons-png.flaticon.com/512/5903/5903939.png"},
  {title: "Rainy", icon: "https://cdn-icons-png.flaticon.com/512/4724/4724091.png"},
  {title: "Thunderstorm", icon: "https://www.iconpacks.net/icons/5/free-lightning-and-rainy-weather-icon-16465-thumb.png"}
];

</script>

<template>

  <section class="mx-auto container">
    <section class="mx-auto container space-y-3 p-5 border border-gray-500 w-80 flex flex-col items-center">
      <template v-for="icon in icons" :key="icon.icon">
        <h2 class="text-2xl">{{icon.title}}</h2>
        <img class="w-32" :src="icon.icon" :alt="icon.title">
      </template>
    </section>
  </section>

</template>

<style scoped>

</style>