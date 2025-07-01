<script setup lang="ts">
import type { TaskInterface } from "@/task";
import { ref } from "vue";

// const tasks = ref<{ text: string; done: boolean }[]>([]);
// Deze Interface vervangt bovenstaande
const tasks = ref<TaskInterface[]>([]);
const taskName = ref("");

//trims input value -> pushes task into array while and sets done to false
// function addTask() {
//   if (taskName.value.trim()) {
//     tasks.value.push({ text: taskName.value, done: false });
//     taskName.value = "";
//   }
// }

function addTask() {
  if (taskName.value.trim()) {
    tasks.value.push({
      name: taskName.value,
      id: tasks.value.length + 1,
      done: false,
      text: taskName.value,
    });
    taskName.value = "";
  }
}
</script>

<template>
  <div class="container-fluid m-5">
    <div class="row justify-content-center align-items-center">
      <input v-model="taskName" placeholder="Add task" />
      <button @click="addTask">Add</button>
      <ul>
        <li v-for="(task, idx) in tasks" :key="idx">
          <!-- de v-model wordt ook meegenomen op andere plekken waar deze task voorkomt -->
          <input type="checkbox" v-model="task.done" />
          <!-- Conditionele If statement voor de CSS -->
          <span :style="{ textDecoration: task.done ? 'line-through' : '' }">{{ task.text }}</span>
        </li>
      </ul>
    </div>
  </div>
</template>

<style scoped></style>
