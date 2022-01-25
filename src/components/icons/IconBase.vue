<template>
  <fa :icon="name" class="icon" size="6x" />
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
  height: 70px;
}
</style>
