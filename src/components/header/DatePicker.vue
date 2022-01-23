<template>
  <div class="block">
    <span class="demonstration">Default</span>
    <el-date-picker v-model="value1" type="date" placeholder="Pick a day">
    </el-date-picker>
  </div>
</template>

<script lang="ts" setup>
import { ref } from "vue";

const value1 = ref("");

const shortcuts = [
  {
    text: "Today",
    value: new Date(),
  },
];

const disabledDate = (time: Date) => {
  return time.getTime() > Date.now();
};

export default {
  components: {
    shortcuts,
    disabledDate,
  },
};
</script>

<style></style>
