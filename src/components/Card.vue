<script setup>
  import { defineProps } from "vue";
  import { useRouter } from "vue-router";

  const router = useRouter();

  const { quiz } = defineProps(["quiz"]);

  const navigateToQuiz = () => {
    router.push(`/quiz/${quiz.id}`);
  };
</script>

<template>
  <div class="card" @click="navigateToQuiz">
    <img :src="quiz.img" alt="" />
    <div class="card-text">
      <h2>{{ quiz.name }}</h2>
      <p>{{ quiz.questions.length }} questions</p>
    </div>
  </div>
</template>

<style scoped>
  /* CARD */
  .card {
    width: 310px;
    overflow: hidden;
    border-radius: 2%;
    box-shadow: 1px 1px 10px rgba(0, 0, 0, 0.1);
    margin-bottom: 35px;
    margin-right: 20px;
    cursor: pointer;
  }

  .card img {
    height: 190px;
    width: 100%;
    margin: 0;
  }

  .card .card-text {
    color: grey;
    padding: 0 5px;
  }

  .card .card-text h2 {
    font-weight: bold;
  }
</style>
