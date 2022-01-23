<template>
  <fa :icon="name" class="icon" size="6x" />
  <p>{{ name }}</p>
</template>

<script setup>
import { defineProps } from "vue";

defineProps({
  name: {
    type: String,
    default: "motorcycle",
  },
});
</script>

<style>
.icon {
  margin-top: 10%;
  height: 80px;
}
</style>
