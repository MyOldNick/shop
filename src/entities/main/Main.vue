<template>
  <div class="main__head">
    <Navbar :buttons="buttonsForNavbar" class="main__navbar"/>
    <div class="main__slider-wrapper">
        <Slider/>
    </div>
  </div>
</template>

<script setup>
//components
import Navbar from '../../ui/navbar/Navbar.vue';
import Slider from '../../ui/slider/Slider.vue';


const buttonsForNavbar = [
    {
        title: 'IPhone'
    },
    {
        title: 'MacBook'
    },
    {
        title: 'IPad'
    },
    {
        title: 'AirPods'
    },
]
</script>

<style scoped>
.main__navbar {
    max-width: 260px;
    min-width: 260px;
}

.main__head {
    width: 100%;
    display: flex;
}

.main__slider-wrapper {
    display: flex;
    justify-content: center;
}
</style>