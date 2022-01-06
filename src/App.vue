<template>
  <div id="app">
    <div class="wrapper">
      <img :src="require(`./assets/images/${images[value]}`)" :alt="value" />
      <input type="range" v-model="value" :max="images.length - 1" />
    </div>
  </div>
</template>

<script>
import { images } from "./images";
export default {
  name: "app",
  data() {
    return {
      value: 0,
      images,
    };
  },
};
</script>
<style>
.wrapper {
  display: inline-flex;
  flex-direction: column;
  margin: 0 auto;
}
img {
  width: 350px;
  height: 350px;
}
</style>
