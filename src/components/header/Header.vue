<template>
  <div class="header">
    <a href=""> <img src="../../assets/nicoblouzlogo.png" alt="logo" /></a>
    <p class="hidden-sm-and-down">Ma candidature chez Motoblouz</p>
    <Icons name="motorcycle" @click="open1" class="icon" />
  </div>
</template>

<script setup>
import "element-plus/theme-chalk/display.css";
import Icons from "../icons/IconBase.vue";
import { ElNotification } from "element-plus";

const open1 = () => {
  ElNotification({
    title: "Mon profil de motard : ",
    message:
      "Bon en fait, je fais essentiellement du vélo... ça y ressemble non ?  ",
    offset: 100,
  });
};
</script>

<style scoped>
@import url("https://fonts.googleapis.com/css2?family=Lato:ital,wght@0,100;0,300;0,400;0,700;1,100;1,300;1,400;1,700&display=swap");

.header {
  display: flex;
  justify-content: space-between;
  align-content: center;
  background: rgb(0, 0, 0);
  color: whitesmoke;
  font-family: "Lato", sans-serif;
}

p {
  font-size: 5vh;
  font-style: italic;
  color: rgb(187, 187, 187);
  margin-top: 1.5%;
}
img {
  height: 100px;
}
.icon {
  margin-top: 1%;
}

.icon:hover {
  cursor: pointer;
}
</style>
