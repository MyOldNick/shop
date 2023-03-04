<template>
  <button :class="['button', { 'button__active': props.active }]"></button>
</template>

<script setup>
//vue
import { defineProps } from "vue";

//props
const props = defineProps({
    active: Boolean
})
</script>

<style scoped>
.button {
  width: 25px;
  height: 25px;
  border-radius: 50%;
  background-color: rgba(217, 217, 217, 0.5);
  transition: 0.3s;
  border: none;
  outline: none;
  cursor: pointer;
}

.button:hover {
  background-color: #ffffff;
  box-shadow: 0px 0px 6px 4px #6473ff;
}

.button__active {
  background-color: #ffffff;
  box-shadow: 0px 0px 6px 4px #6473ff;
}
</style>