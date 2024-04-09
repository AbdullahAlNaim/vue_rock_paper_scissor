<script setup>
import Moves from "./Moves.vue"

</script>

<template>
  <section class="results">
    <h2>Results</h2>
    <p >{{ win }}</p>
  </section>
</template>

<style scoped>
.results {
  background-color: aliceblue;
  width: 500px;
  margin: auto;
  text-align: center;
  border-radius: 10px;
}
</style>