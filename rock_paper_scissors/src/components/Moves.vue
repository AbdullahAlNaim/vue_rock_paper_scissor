<script setup>
import moveData from "../data/moves.json"
import Results from "./Results.vue"
import { ref } from "vue"

const moves = ref(moveData)
let kda = []

function stopReload(input) {
  let num = Math.floor(Math.random() * 3)
  let ai = moves.value[num]["name"]

  if (input === ai) {
    kda.push('ITS A TIE')
  } else if (input === 'rock' && ai === 'paper') {
    kda.push('AI WINS')
  } else if (input === 'rock' && ai === 'scissor') {
    kda.push('You WIN')
  } else if (input === 'paper' && ai === 'scissor') {
    kda.push('AI WINS')
  } else if (input === 'paper' && ai === 'rock') {
    kda.push('You WINS')
  } else if (input === 'scissor' && ai === 'rock') {
    kda.push('AI WINS')
  } else if (input === 'scissor' && ai === 'paper') {
    kda.push('You WINS')
  }
  console.log(kda)
}


</script>

<template>
    <section class="moves">
      <article v-for="move in moves">
        <h2 >{{ move.name }}</h2>
          <div class="place">
            <img @click="stopReload(move.name)" :src="move.image" alt=""> 
          </div>
     </article>
    </section>
    <section class="results">
      <h2>Results</h2>
      <p></p>
    </section>
</template>

<style scoped>
/* content */
.moves {
  display: flex;
  justify-content: center;
}

article {
  margin: auto;
  background-color: aliceblue;
  width: 300px;
  border-radius: 10px;
}

article h2 {
  text-align: center;
  margin: auto;
}

.place {
  padding: 10px;
  margin: 0;
  height: 200px;
  display: flex;
  justify-content: center;
}

img {
  width: 200px;
  height: 200px;
}

.results {
  background-color: aliceblue;
  width: 500px;
  margin: auto;
  text-align: center;
  border-radius: 10px;
}
</style>