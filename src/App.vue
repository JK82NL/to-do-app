<script setup lang="ts">
import Counter from "./components/Counter.vue";
import { ref } from "vue";

const counters = ref<string[]>([]);
const newName = ref("");

function handleThreshold(value: string) {
  alert(value);
}

function addCount() {
  counters.value.push(newName.value);
  newName.value = "";
}
</script>

<template>
  <h1>Dit is mijn teller</h1>
  <!-- <input type="text" v-model="newName" />{{ newName }} UPDATE GELIJK-->
  <input type="text" v-model="newName" />
  <button @click="addCount">Nieuwe teller</button>
  <!-- <Counter :name="'Koolhydraten' + 'iets anders'" @threshold-reached="handleThreshold"></Counter>
  <Counter name="Sugars"></Counter> -->
  <div v-for="count in counters">
    <Counter :name="count" @threshold-reached="handleThreshold"></Counter>
  </div>
</template>

<style scoped></style>
