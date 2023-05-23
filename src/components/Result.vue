<script setup>
import { RouterLink } from 'vue-router';

const { numberOfCorrectAnswers, quizQuestionLength } = defineProps([
  'quizQuestionLength',
  'numberOfCorrectAnswers',
]);
</script>

<template>
  <div class="results">
    <p>Your Results...</p>
    <h1>{{ numberOfCorrectAnswers }}/{{ quizQuestionLength }}</h1>
    <RouterLink to="/" class="router-btn">Go Back</RouterLink>
  </div>
</template>

<style scoped>
.results {
  text-align: center;
  padding: 100px 0;
}

p {
  font-size: 25px;
}

h1 {
  font-size: 80px;
}

.router-btn {
  display: inline-block;
  text-decoration: none;
  padding: 10px 20px;
  background-color: #fffacd;
  font-size: 18px;
  color: inherit;
  border-radius: 5px;
  margin-top: 20px;
  transition: transform 0.2s;
}

.router-btn:hover {
  transform: translateY(-5px);
}
</style>
