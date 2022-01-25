<template>
  <GoogleMap
    api-key="AIzaSyAsAipAYPzUlS7sENjh-L5QqpCsuDTnG6w"
    style="width: 100%; height: 500px"
    :center="center"
    :zoom="15"
  >
    <Marker :options="{ position: center }" />
    <Marker
      :key="marker.id"
      v-for="marker in markers"
      :position="marker.position"
    />
  </GoogleMap>
</template>

<script>
/* eslint-disable no-undef*/
import { defineComponent } from "vue";
import { GoogleMap, Marker } from "vue3-google-map";

export default defineComponent({
  components: { GoogleMap, Marker },
  setup() {
    const center = { lat: 50.447262, lng: 2.9027 };
    //const point = { lat: 50.473229, lng: 2.951438 };
    const markers = [
      {
        id: "dfsldjl3r",
        position: {
          lat: 50.473229,
          lng: 2.951438,
        },
      },
    ];
    return { center, markers };
  },
});
</script>
<style></style>
