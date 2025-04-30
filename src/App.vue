<script setup>
  import { RouterView } from "vue-router";
  import QuizesView from "./views/QuizesView.vue";
</script>

<template>
  <div class="main">
    <div class="container"></div>
    <RouterView />
  </div>
</template>

<style scoped>
  .main {
    height: 100vh;
    width: 100vw;
    padding: 5px;
    background-color: aliceblue;
  }
  .container {
    max-width: 1000px;
    margin: 0 auto;
  }
</style>
