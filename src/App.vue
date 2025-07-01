<script setup lang="ts">
import Counter from "./components/Counter.vue";
import MainHeader from "./components/MainHeader.vue";
import TaskList from "./components/TaskList.vue";
</script>

<template>
  <MainHeader />

  <TaskList />
  <!-- <input type="text" v-model="giveName" />
    <button @click="addTask()">Add Task</button> -->

  <div>
    <h3>Icons</h3>
    <ul>
      <i class="bi bi-list-task"></i>
    </ul>
  </div>
</template>

<style scoped>
/* .container {
  display: flex;
  justify-content: center;
  align-items: center;
  margin-bottom: 15px;
}

header {
  background: lightcoral;
  width: 700px;
  border-top-left-radius: 5%;
  border-top-right-radius: 5%;
  border-bottom-left-radius: 5%;
  border-bottom-right-radius: 5%;
}

h1 {
  font-size: xx-large;
  font-family: "Segoe UI", Tahoma, Geneva, Verdana, sans-serif;
}

.task-list-box {
  display: border-box;
  max-width: 25vw;
  height: fit-content;
  background: lightcyan;
} */
</style>
