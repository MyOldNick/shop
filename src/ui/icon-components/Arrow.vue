<template>
  <svg
    width="11"
    height="20"
    viewBox="0 0 11 20"
    fill="none"
    xmlns="http://www.w3.org/2000/svg"
    :class="[`icon icon__${props.color}`]"
  >
    <line
      y1="-0.5"
      x2="13.1708"
      y2="-0.5"
      transform="matrix(-0.728353 -0.685202 0.948393 -0.317099 10.593 9.02466)"
      stroke="#CECECE"
    />
    <line
      y1="-0.5"
      x2="13.2312"
      y2="-0.5"
      transform="matrix(-0.653717 0.756739 -0.916985 -0.398922 9.64951 8.69565)"
      stroke="#CECECE"
    />
  </svg>
</template>

<script setup>
//vue
import { defineProps } from "vue";

const props = defineProps({
  size: String,
  color: String,
});
</script>

<style scoped>

.icon {
    transition: .3s;
    
}

.icon__default  line {
    stroke: #CECECE;
}

.icon__blue line {
    stroke: #52C1FF;
}
</style>