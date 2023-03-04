<template>
  <button :class="[`button button__${props.style} button__${props.size}`]">
    <slot />
  </button>
</template>

<script setup>
//vue
import { defineProps } from "vue";

//props
const props = defineProps({
  size: {
    type: String,
    default: "default",
  },
  style: {
    type: String,
    default: "default",
  },
});
</script>

<style scoped>
.button {
  outline: none;
  border: none;
  min-height: 40px;
  min-width: 130px;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 16px;
  line-height: 20px;
}
.button__default {
  border-radius: 20px;
  background: #6473ff;
  color: #ffffff;
}

.button__outlined {
  background: #ffffff;
  border: 1px solid #878585;
  border-radius: 20px;
  color: #333333;
}
</style>