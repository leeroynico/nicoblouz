<template>
  <div>
    <Header />
    <Profil />
    <Competence />
    <div class="contact">
      <Contact />
    </div>
  </div>
</template>

<script>
import Header from "./components/header/Header.vue";
import Profil from "./components/Profil.vue";
import Contact from "./components/Contact.vue";
import Competence from "./components/competences/Competences.vue";
export default {
  name: "App",
  components: {
    Header,
    Profil,
    Competence,
    Contact,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;1,100;1,300;1,400;1,700&family=Roboto:ital,wght@0,300;0,400;1,100;1,300&display=swap");

#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  width: 100%;
}
* {
  margin: 0;
}

.contact {
  margin-top: 60px;
}
</style>
