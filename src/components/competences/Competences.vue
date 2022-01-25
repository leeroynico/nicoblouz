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
    name: " react",
    img: "../../assets/react.png",
    stars: 5,
    halfStars: false,
  },
  {
    id: 1,
    name: " react",
    img: "../../assets/react.png",
    stars: 4,
    halfStars: false,
    bannier: "NOUVEAUTE",
  },
  {
    id: 2,
    name: " vue",
    img: "../../assets/react.png",
    stars: 2,
    halfStars: true,
  },
];
</script>

<style scoped>
h2 {
  font-family: "Lato", sans-serif;
  font-size: 3rem;
  margin-top: 5px;
  margin-bottom: 5px;
  text-align: center;
}
h3 {
  font-family: "Lato", sans-serif;
  font-size: 1.2rem;
  margin-top: 1px;
  color: grey;
  text-transform: uppercase;
  text-align: center;
}
.competence {
  margin-top: 30px;
  display: flex;
  flex-direction: row;
}
</style>
