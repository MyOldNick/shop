<template>
  <div class="slider">
    <img
      v-for="{ id, src } in imagesList"
      :key="id"
      :src="src"
      alt="slider 1"
    />
    <div class="slider__btns-wrapper">
        <SliderButton v-for="({ id }) in imagesList" :key="id" :active="activeSlide === id ? true : false" class="slider__button"/>
    </div>
  </div>
</template>

<script setup>
//vue
import { ref, defineProps } from "vue";
//components
import SliderButton from "../buttons/SliderButton.vue"; 
//images
import SliderImage1 from "../../assets/images/slider1.svg";

//state
const activeSlide = ref(1)
//в будущем картинки должны приходить из сервера, поэтому реактивная херня
const imagesList = ref([
  {
    id: 1,
    src: SliderImage1,
  },
  {
    id: 2,
    src: SliderImage1,
  },
]);
</script>

<style scoped>
.slider {
  display: flex;
  overflow: hidden;
  position: relative;
}

.slider img {
    width: max-content;
}

.slider__btns-wrapper {
    width: 100%;
    position: absolute;
    display: flex;
    justify-content: center;
    bottom: 20px;
}

.slider__button {
    margin: 0 12px;
}
</style>