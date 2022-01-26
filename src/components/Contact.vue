<template>
  <h2>Mes infos</h2>
  <h3>ou me trouver</h3>
  <div class="container">
    <div class="left">
      <p>
        Les deux points représentent pour l'un l'endroit où je vis et l'autre
        l'adresse de votre Paddock. Je pourrai ainsi venir en moto sans
        difficulté (même si ma moto n'a pas de moteur et que je pédale avec ...)
      </p>
      <GoogleMap
        api-key="AIzaSyAsAipAYPzUlS7sENjh-L5QqpCsuDTnG6w"
        :center="center"
        :zoom="12"
        class="map"
      >
        <Marker :options="{ position: center, label: labelHome }" />
        <Marker :options="{ position: office, label: labelOffice }" />
      </GoogleMap>
    </div>

    <div class="right">
      <div class="card">
        <p>Nicolas leroy</p>
        <p>développeur web Front-End</p>
        <a href="mailto:nicoleroydev@gmail.com">
          <p>nicoleroydev@gmail.com</p></a
        >
        <p>06 17 52 84 97</p>
      </div>
    </div>
  </div>
</template>

<script>
/* eslint-disable no-undef*/
import { defineComponent } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";

export default defineComponent({
  components: { GoogleMap, Marker },
  setup() {
    const labelHome = {
      text: "home",
      color: "white",
      fontWeight: "bolder",
    };
    const labelOffice = {
      text: "paddock",
      color: "white",
      fontWeight: "bolder",
    };

    const center = { lat: 50.447262, lng: 2.9027 };
    const office = {
      lat: 50.473229,
      lng: 2.951438,
    };

    return { center, office, labelHome, labelOffice };
  },
});
</script>
<style scoped>
.container {
  display: flex;
  justify-content: space-evenly;
  align-items: center;
  gap: 50px;
  margin-bottom: 50px;
}

p {
  font-family: "Roboto", sans-serif;
  font-size: 3vh;
}

.map {
  height: 350px;
}

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
.card {
  padding-left: 2%;
  padding-right: 2%;
  background-color: rgba(0, 82, 235, 0.56);
  border-radius: 12px;
  border: 4px solid rgb(1, 53, 99);
}

/* .right {
} */

.left {
  max-width: 800px;
}
</style>
