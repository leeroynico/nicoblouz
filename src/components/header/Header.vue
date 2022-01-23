<template id="container">
  <div class="header">
    <img src="../../assets/nicoblouzlogo.png" alt="logo" />
    <DatePicker></DatePicker>
  </div>
</template>

<script>
import DatePicker from "./DatePicker.vue";

export default {
  name: "Header",
  components: {
    DatePicker,
  },
  props: {},
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;1,100;1,300;1,400;1,700&display=swap");

.header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  background: black;
  height: 20vh;
  color: whitesmoke;
  font-family: "Lato", sans-serif;
}

img {
  height: 100px;
}
</style>
