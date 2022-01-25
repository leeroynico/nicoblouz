<template>
  <h2>Ma selection de compétences</h2>
  <h3>Le meilleur de mes compétences</h3>
  <ol>
    <li v-for="competence in competences" :key="competence">
      {{ competence.name }}
    </li>
  </ol>
</template>

<script setup>
const competences = [
  { name: " JavaScript" },
  { name: " Vue" },
  { name: " php" },
];
</script>

<style scoped>
h2 {
  font-family: "Lato", sans-serif;
  font-size: 3rem;
  margin-top: 5px;
  margin-bottom: 5px;
}
h3 {
  font-family: "Lato", sans-serif;
  font-size: 1.2rem;
  margin-top: 1px;
  color: grey;
  text-transform: uppercase;
}
</style>
