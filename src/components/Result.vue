<script setup>
  import { defineProps } from "vue";
  import { RouterLink } from "vue-router";

  const { quizQuestionLength, numberOfCorrectAnswers } = defineProps([
    "quizQuestionLength",
    "numberOfCorrectAnswers",
  ]);
</script>

<template>
  <div class="results">
    <p>Your Results ...</p>
    <h1>{{ numberOfCorrectAnswers }} / {{ quizQuestionLength }}</h1>
    <RouterLink to="/">Go Back</RouterLink>
  </div>
</template>

<style scoped>
  .results {
    text-align: center;
    padding: 100px 0;
  }

  p {
    font-size: 25px;
    color: black;
  }

  h1 {
    font-size: 80px;
    font-weight: bold;
    color: black;
  }
</style>
