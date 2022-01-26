<template>
  <h2>Ma selection de compétences</h2>
  <h3>Le meilleur de mes compétences</h3>
  <div class="competence">
    <div v-for="item in competences" :key="item.id">
      <Competence
        :name="item.name"
        :img="item.img"
        :stars="item.stars"
        :halfStars="item.halfStars"
        :bannier="item.bannier"
      />
    </div>
  </div>
</template>

<script setup>
import Competence from "./Competence.vue";

const competences = [
  {
    id: 1,
    name: "react",
    img: "react.png",
    stars: 5,
    halfStars: false,
  },
  {
    id: 1,
    name: "vue",
    img: "vue.png",
    stars: 3,
    halfStars: false,
    bannier: "NOUVEAUTE",
  },
  {
    id: 2,
    name: "symfony",
    img: "symfony.png",
    stars: 2,
    halfStars: true,
  },
  {
    id: 2,
    name: "api platform",
    img: "apiPlatform.png",
    stars: 4,
  },
];
</script>

<style scoped>
h2,
h3 {
  font-family: "Lato", sans-serif;
  text-align: center;
}

h2 {
  font-size: 3rem;
  margin-top: 5px;
  margin-bottom: 5px;
}
h3 {
  font-size: 1.2rem;
  margin-top: 1px;
  color: grey;
  text-transform: uppercase;
}
.competence {
  margin-top: 30px;
  display: flex;
  flex-direction: row;
  justify-content: space-evenly;
}
</style>
