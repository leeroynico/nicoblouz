<template>
  <div class="card">
    <img :src="require(`@/assets/${img}`)" alt="react" />
    <div class="banniere">{{ bannier }}</div>
    <h4>{{ name }}</h4>
    <div class="stars">
      <div v-for="index in stars" :key="index">
        <fa :icon="['fa', 'star']" size="1x" />
      </div>
      <div v-if="halfStars">
        <fa :icon="['fa', 'star-half-alt']" size="1x" />
      </div>
    </div>
  </div>
</template>

<style scoped>
.card {
  border-radius: 40px / 34px;
  width: 300px;
  display: flex;
  flex-direction: column;
  align-items: center;
}

img {
  width: 60%;
  max-height: 150px;
}
.banniere {
  margin-top: 15px;
  background: red;
  width: 80%;
  display: flex;
  justify-content: center;
  font-family: sans-serif;
  color: whitesmoke;
  font-size: 1.2rem;
  font-weight: bolder;
}

p {
  margin-top: auto;
  margin-bottom: auto;
  text-transform: uppercase;
}
.stars {
  margin-top: 8px;
  display: flex;
}

h4 {
  margin: 0;
  margin-top: 10px;
  text-transform: uppercase;
}
</style>

<script setup>
import { defineProps } from "vue";

defineProps({
  name: {
    type: String,
    default: "react",
    required: true,
  },
  img: {
    type: String,
    default: "react.png",
  },
  stars: {
    type: Number,
    default: 4,
  },
  halfStars: {
    type: Boolean,
    default: false,
  },
  bannier: {
    type: String,
    default: "BON PLAN",
  },
});
</script>
