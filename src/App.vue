<template>
  <div>
    <!-- TODO: подключить роутер и убрать ето безобращие -->
    <Header/>
    <Main/>
  </div>
</template>
 
<script setup>
//pages
import Main from './entities/main/Main.vue';
//components
import Header from './ui/header/Header.vue';
</script>

<style scoped>
</style>
