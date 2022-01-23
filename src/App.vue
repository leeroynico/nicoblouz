<template>
  <div class="container">
    <Header />
    <Profil />
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
