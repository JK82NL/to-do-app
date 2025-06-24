<script setup lang="ts">
import { ref } from "vue";

defineProps<{
  name?: string;
}>();
// name?: geeft aan dat een naam optioneels is.
const emit = defineEmits<{
  (event: "thresholdReached", value: string): void;
}>();

const count = ref(0);

function updateCount(value: number) {
  count.value += value;

  if (count.value > 10) {
    emit("thresholdReached", "Hyper Bereikt!");
  }
}
</script>

<template>
  <p>{{ name }}</p>
  <div>{{ count }}</div>
  <button @click="updateCount(1)">+</button>
  <button @click="updateCount(-1)">-</button>
  <button v-if="count !== 0" @click="count = 0">Reset</button>
</template>

<style scoped></style>
