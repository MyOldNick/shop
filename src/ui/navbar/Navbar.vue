<template>
  <div class="navbar">
    <NavbarButton v-for="({ title }, index) in buttons" :key="index">{{ title }}</NavbarButton>
  </div>
</template>

<script setup>
//vue
import { defineProps } from 'vue';
//components
import NavbarButton from '../buttons/NavbarButton.vue';


//props
const props = defineProps({
    buttons: Array
})

</script>

<style scoped>

</style>