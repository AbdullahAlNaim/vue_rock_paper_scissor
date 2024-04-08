<script setup>
// import { ref } from "vue"

const moves = [
  {
    "name": "rock",
    "image": "./src/assets/rock.png",
  },
  {
    "name": "paper",
    "image": "./src/assets/p6.png",
  },
  {
    "name": "scissor",
    "image": "./src/assets/scis.png",
  }
]



</script>

<template>
<section class="moves">
      <article v-for="move in moves">
        <h2 >{{ move.name }}</h2>
          <div class="place">
            <a href="">
              <img :src="move.image" alt="">
            </a>
        </div>
     </article>
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
}

img {
  width: 200px;
  height: 200px;
}

a {
  display: flex;
  justify-content: center;
}
</style>