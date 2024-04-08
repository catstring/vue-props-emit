<script setup>
import { ref } from 'vue'

defineProps({
  name: String,
  department: String,
  salary: Number,
  position: Number
})
</script>

<template>
  <div class="container">
    <h2>name: {{ name }}</h2>
    <p>department: {{ department }}</p>
    <p>salary: {{ salary }}</p>
    <p>position: {{ position }}</p>
  </div>
</template>

<style scoped>

</style>
