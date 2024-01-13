<script setup>
import Reactivity from "./components/Reactivity.vue";
import Task from "./components/Task.vue";
import ClassBinding from "./components/Practice/ClassBinding.vue";
import StyleBinding from "./components/Practice/StyleBinding.vue";
import Loop from "./components/Practice/Loop.vue";
import LoopArray from "./components/Practice/LoopArray.vue";
import LoopMember from "./components/Practice/LoopMember.vue";
import LoopWeather from "./components/Practice/LoopWeather.vue";
import Event from "./components/Practice/Event.vue";
import EventLoop from "./components/Practice/EventLoop.vue";
import EventImage from "./components/Practice/EventImage.vue";


const numbers = [1, 2, 3, 4, 5, 6, 7];

const todos = [
  {id: 1, task: "Taking vue js class", status: "In Progress"},
  {id: 2, task: "Upload source code", status: "Pending"},
  {id: 3, task: "Ready Quiz Question", status: "Done"},
  {id: 4, task: "Taking vue js class", status: "In Progress"},
]

const persons = {
  name: "John Smith",
  age: 30,
  Gender: "Male",
  occupation: "Vue JS Developer"
}

</script>

<template>

  <p v-for="(number,index) in numbers" :key="index" >{{number}}</p>

  <h1>In Progress</h1>
  <ul>
    <template v-for="todo in todos" :key="todo.id">
      <li v-show="'In Progress' === todo.status">
        {{todo.task}}
      </li>
    </template>
  </ul>

  <h1>Pending</h1>
  <ul>
    <template v-for="todo in todos" :key="todo.id">
      <li v-show="'Pending' === todo.status">
        {{todo.task}}
      </li>
    </template>
  </ul>

  <h1>Done</h1>
  <ul>
    <template v-for="todo in todos" :key="todo.id">
      <li v-show="'Done' === todo.status">
        {{todo.task}}
      </li>
    </template>
  </ul>



  <ul>
    <template v-for="todo in todos" :key="todo.id">
      <li class="list" :class="{'line':('Done' === todo.status)}">
        {{todo.task}}
      </li>
    </template>
  </ul>


  <h1>Person</h1>
  <p v-for="(person,key,index) in persons" :key="index">{{key +":"+person}}</p>


  <Reactivity/>

  <Task/>

<ClassBinding/>

  <StyleBinding/>

  <Loop/>

  <LoopArray/>

  <LoopMember/>

  <LoopWeather/>

  <Event/>

  <EventLoop/>

  <EventImage/>


</template>

<style scoped>

.line{
  text-decoration: line-through;
}

</style>
