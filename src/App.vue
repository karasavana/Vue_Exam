<template>
  <div>
    <h2>Student List</h2>
    <ul>
      <li v-for="(student, index) in students" :key="index">{{ student }}</li>
    </ul>

    <!-- Pass the first student as username prop -->
    <Greeting :username="students[0]" />
    <Students />
  </div>
</template>

<script setup>
import { ref } from 'vue';
import Greeting from './components/Greeting.vue';
import Students from './components/Students.vue'; // renamed to Students.vue

const students = ref(['Alice', 'Bob', 'Charlie']);
</script>
