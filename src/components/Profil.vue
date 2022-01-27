<template>
  <div class="container">
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
            <fa :icon="['fab', 'linkedin']" class="icon"
          /></a>
        </div>
        <div class="socialItem">
          <label>github</label>
          <a href="https://github.com/leeroynico/" target="blank">
            <fa :icon="['fab', 'github']" class="icon"
          /></a>
        </div>
        <div class="socialItem">
          <label>portfolio react</label>
          <a href="https://portfolionicoleroy.netlify.app" target="blank">
            <fa :icon="['fa', 'address-card']" class="icon" />
          </a>
        </div>
      </div>
    </div>
  </div>
</template>

<script></script>

<style scoped>
.container {
  background-image: url("https://res.cloudinary.com/leeroynico/image/upload/c_scale,w_1452/v1643315479/samples/profil_xhx7ws.jpg");
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
}
p {
  font-family: "Roboto", sans-serif;
  font-size: 4.5vh;
  color: rgb(187, 187, 187);
}
.card {
  margin-top: 2%;
  margin-bottom: 2%;
  padding-left: 2%;
  padding-right: 2%;
  width: 70%;
  backdrop-filter: blur(2px) saturate(78%);
  -webkit-backdrop-filter: blur(2px) saturate(78%);
  background-color: rgba(17, 25, 40, 0.56);
  border-radius: 12px;
  border: 1px solid rgba(255, 255, 255, 0.125);
}
.social {
  margin-top: 2%;
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
.icon {
  font-size: 20rem;
}

@media (max-width: 850px) {
  h1 {
    font-size: 1.8rem;
  }
  p {
    font-size: 1.5rem;
  }
  .icon {
    font-size: 3rem;
  }
  label {
    font-size: 0.8rem;
  }
  .social {
    margin-top: 5%;
  }
  .card {
    width: 90%;
  }
  .social {
    margin-bottom: 0;
  }
}
</style>
