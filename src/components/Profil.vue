<template>
  <div class="container">
    <!-- <img src="../assets/profil.jpg" alt="profil" /> -->
    <div class="card">
      <h1>mon profil</h1>
      <p>
        Je suis un développeur Front-End, ayant beaucoup d'appétence pour le
        Javascript (notamment React). Ayant vu votre annonce et vu Vue.js, j'ai
        donc réalisé ce mini projet afin de vous montrer mon envie et mon désir
        de monter en compétence sur cette technologie.
      </p>
      <h1>mes réseaux sociaux</h1>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.container {
  background-image: url("../assets/profil.jpg");
  height: 80vh;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: center;
}

h1 {
  font-family: "Lato", sans-serif;
  font-size: 4rem;
  color: whitesmoke;
  margin: 0;
  margin-left: 50px;
}
p {
  font-size: 4.5vh;
  color: rgb(187, 187, 187);
  margin-left: 5%;
  margin-right: 5%;
  text-align: justify;
}
.card {
  margin-top: 2%;
  margin-bottom: 2%;
  width: 70%;
  backdrop-filter: blur(2px) saturate(78%);
  -webkit-backdrop-filter: blur(2px) saturate(78%);
  background-color: rgba(17, 25, 40, 0.56);
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.125);
}
</style>
