<template>
  <h2>Mes infos</h2>
  <h3>et ma localisation</h3>
  <el-row :gutter="20" justify="space-around">
    <el-col :md="22" :lg="15">
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
        <Marker
          :options="{ position: office, label: labelOffice }"
        /> </GoogleMap
    ></el-col>
    <el-col :xs="16" :sm="12" :md="10" :lg="7">
      <el-card shadow="always" class="card">
        <el-avatar
          src="https://res.cloudinary.com/leeroynico/image/upload/c_scale,w_327/v1643300610/samples/business_xpsbkd.png"
          class="avatar"
        ></el-avatar>
        <h2>Nicolas leroy</h2>
        <p>développeur web Front-End</p>
        <div class="inline">
          <fa :icon="['fa', 'envelope']" size="1x" />
          <span></span>
          <p>nicoleroydev@gmail.com</p>
        </div>
        <div class="inline">
          <fa :icon="['fa', 'phone-square-alt']" size="1x" />
          <span></span>
          <p>06 17 52 84 97</p>
        </div>
        <el-button type="info" plain class="button" size="large" round
          >MON CV
        </el-button>
      </el-card>
    </el-col>
  </el-row>
</template>

<script>
/* eslint-disable no-undef*/
import { defineComponent } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";
import { ElCard, ElAvatar, ElButton, ElRow, ElCol } from "element-plus";

export default defineComponent({
  components: { GoogleMap, Marker, ElCard, ElAvatar, ElButton, ElRow, ElCol },
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
  margin-bottom: 2%;
}
.button {
  margin-top: 3%;
  color: rgb(0, 0, 0);
}
.inline {
  display: flex;
  align-items: center;
  justify-content: start;
}
.inline > p {
  font-size: 1.1rem;
  margin-left: 5%;
}
@media (max-width: 850px) {
  p {
    font-size: 1.2rem;
    margin: 5px;
    margin-bottom: 20px;
  }
  .card {
    margin-top: 5%;
  }
  .avatar {
    width: 98%;
  }
}
</style>
