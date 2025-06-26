<script setup lang="ts">
import ToDoListInput from "./components/ToDoListInput.vue";
import { ref } from "vue";

// import Counter from "./components/Counter.vue";
// import { ref } from "vue";

// const counters = ref<string[]>([]);
// const newName = ref("");

const giveName = ref<string[]>();
const addTask = ref("");

function addTaskList() {
  giveName.value.push(giveName.value);
}
// function handleThreshold(value: string) {
//   alert(value);
// }

// function addCount() {
//   counters.value.push(newName.value);
//   newName.value = "";
// }
</script>

<template>
  <header class="container"><h1>To-do App</h1></header>

  <div class="container">
    <input type="text" v-model="giveName" />
    <button @click="addTask">Add Task</button>
  </div>
  <div class="container">{{ giveName }}</div>

  <!--  -->
  <!-- <h1>Dit is mijn teller</h1> -->
  <!-- <input type="text" v-model="newName" />{{ newName }} UPDATE GELIJK-->
  <!-- <input type="text" v-model="newName" /> -->
  <!-- <button @click="addCount">Nieuwe teller</button> -->
  <!-- <Counter :name="'Koolhydraten' + 'iets anders'" @threshold-reached="handleThreshold"></Counter>
  <Counter name="Sugars"></Counter> -->
  <!-- <div v-for="count in counters"> -->
  <!-- <Counter :name="count" @threshold-reached="handleThreshold"></Counter> -->
  <!-- </div> -->
</template>

<style scoped>
.container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin: 15px;
}

header {
  background: lightcoral;
}

h1 {
  font-size: xx-large;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}
</style>
