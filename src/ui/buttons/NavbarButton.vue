<template>
  <button @mouseover="onHover" @mouseleave="offHover" class="button">
    <slot />
    <Arrow :color="hoverForSVG ? 'blue' : 'default'" />
  </button>
</template>

<script setup>
//vue
import { ref } from "vue";
//icons
import Arrow from "../icon-components/Arrow.vue";

const hoverForSVG = ref(false);

//methods
const onHover = () => (hoverForSVG.value = true);
const offHover = () => (hoverForSVG.value = false);
</script>

<style scoped>
.button {
  outline: none;
  border: none;
  width: 100%;
  min-height: 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding-left: 24px;
  padding-right: 24px;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 24px;
  line-height: 29px;
  color: #333333;
  background-color: #ffffff;
  cursor: pointer;
  transition: 0.3s;
}

.button:hover {
  color: #52c1ff;
  background-color: #f9f9f9;
}
</style>