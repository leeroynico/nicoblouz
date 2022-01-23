<template id="container">
  <div class="header">
    <img src="../../assets/nicoblouzlogo.png" alt="logo" />
    <p>ma candidature chez Motoblouz</p>
    <div>
      <Icons icon-name="write"><icon-write /></Icons>
    </div>
  </div>
</template>

<script>
import Icons from "../icons/IconBase.vue";
export default {
  components: {
    Icons,
  },
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;1,100;1,300;1,400;1,700&display=swap");

.header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  background: black;
  color: whitesmoke;
  font-family: "Lato", sans-serif;
}
p {
  font-size: 5vh;
  font-style: italic;
  color: rgb(187, 187, 187);
}

img {
  height: 100px;
}
</style>
