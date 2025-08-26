<script setup>
import { ref } from 'vue';

const students = ref([
  { name: 'Kara Savana Sajol', score: 100 },
  { name: 'Krissa Malas', score: 80 },
  { name: 'Jane Doe', score: 25 },
  { name: 'Maria Garcia', score: 50 },
]);
</script>

<template>
  <div>
    <h2>Name List</h2>
    <ul>
      <li 
        v-for="(student, index) in students" 
        :key="index" 
        :class="{ highlight: student.score >= 70 }"
      >
        {{ student.name }} - Score: {{ student.score }}
      </li>
    </ul>
  </div>
</template>

<style scoped>
.highlight {
  color: green;
  font-weight: bold;
}
</style>
