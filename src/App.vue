<script setup lang="ts">
import { ref } from "vue";
const message = "number";
const number = ref(10);
const color = ref("color_red");
const disable = ref(false);

function change_color() {
  color.value = "green";
  disable.value = true;
  number.value = 10;
}
</script>

<template>
  <div>
    <h1 :id="color">{{ message }} : {{ number }}</h1>
    <button @click="change_color" :disabled="disable">click</button>
    <div class="background main">abc</div>
  </div>
</template>

<style scoped>
#color_red {
  color: rgb(255, 0, 0);
}

#blue {
  color: aqua;
}
</style>
