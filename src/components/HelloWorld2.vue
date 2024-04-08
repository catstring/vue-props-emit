<script setup>
import { ref } from 'vue'

defineProps({
  name: String,
  department: String,
  salary: Number,
  position: Number
})

// const emit = defineEmits(['destroy'])
// const destroy = (position) => emit('destroy', position)
</script>

<template>
    <div class="container">
      <h2>name: {{ name }}</h2>
      <p>department: {{ department }}</p>
      <p>salary: {{ salary }}</p>
      <p>position: {{ position }}</p>
      <button @click="$emit('destroy', position)">Delete</button>
      <!-- <button @click="destroy">Delete</button> -->
    </div>
</template>

<style scoped>

</style>
