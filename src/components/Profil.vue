<template>
  <div class="container">
    <!-- <img src="../assets/profil.jpg" alt="profil" /> -->
    <div class="card">
      <h1>Mon profil</h1>

      <p>
        Je suis un développeur Front-End, ayant beaucoup d'appétence pour le
        Javascript (notamment React). En apercevant votre annonce et vu Vue.js,
        j'ai décider de réaliser ce projet en Vue.js (le code source est
        <a href="https://github.com/leeroynico/nicoblouz" target="blank"> ici</a
        >) afin de vous montrer mon envie de monter en compétence sur cette
        technologie.
      </p>

      <h1>Mes réseaux sociaux</h1>
      <div class="social">
        <div class="socialItem">
          <label>linkedin</label>
          <a href="https://www.linkedin.com/in/nico-leeroy/" target="blank">
            <fa :icon="['fab', 'linkedin']" size="6x"
          /></a>
        </div>
        <div class="socialItem">
          <label>github</label>
          <a href="https://github.com/leeroynico/" target="blank">
            <fa :icon="['fab', 'github']" size="6x"
          /></a>
        </div>
        <div class="socialItem">
          <label>portfolio react</label>
          <a href="https://portfolionicoleroy.netlify.app" target="blank">
            <fa :icon="['fa', 'address-card']" size="6x" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.container {
  background-image: url("../assets/profil.jpg");
  height: 85vh;
  background-repeat: no-repeat;
  background-size: cover;
  display: flex;
  justify-content: center;
  color: whitesmoke;
}

h1 {
  font-family: "Lato", sans-serif;
  font-size: 4rem;
  color: whitesmoke;
  margin: 0;
  margin-left: 50px;
}
p {
  font-family: "Roboto", sans-serif;
  font-size: 4.5vh;
  color: rgb(187, 187, 187);
  margin-left: 5%;
  margin-right: 5%;
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
.social {
  display: flex;
  justify-content: space-around;
}
.socialItem {
  display: flex;
  flex-direction: column;
  align-items: center;
}
a {
  color: whitesmoke;
}
</style>
