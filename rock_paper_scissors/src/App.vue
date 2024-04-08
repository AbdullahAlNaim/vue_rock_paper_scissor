<script setup>
// import { ref } from "vue"
import Moves from "./components/Moves.vue"
import Results from "./components/Results.vue"


</script>

<template>
  <main>
    <h1>Rock Paper Scissors</h1>
    <Moves />
    <Results />
  </main>
</template>

<style scoped>
main {
  background-image: url("./assets/back.jpg");
  background-size: cover;
  background-position: center center;
  background-repeat: no-repeat;
  width: 81em;
  height: 63em;
  margin: 0 auto;
  padding: 0;
}

h1 {
  display: flex;
  justify-content: center;
  margin-top: 0;
  margin-bottom: 20px;
}
</style>
