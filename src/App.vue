<template>
  <div class="container">
    <Header />
    <Profil />

    <p>
      Lorem ipsum dolor sit amet consectetur adipisicing elit. Corrupti,
      quaerat. Illo sapiente debitis ipsam ab voluptates, nobis, perferendis
      aspernatur similique eum voluptatum velit, consequatur eius maiores facere
      tempore inventore quas!
    </p>
  </div>
</template>

<script>
import Header from "./components/header/Header.vue";
import Profil from "./components/Profil.vue";
export default {
  name: "App",
  components: {
    Header,
    Profil,
  },
};
</script>

<style scoped>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
}
.container {
  background: grey;
}
</style>
