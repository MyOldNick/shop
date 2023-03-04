<template>
  <div class="header">
    <div>
        <img :src="Logo" alt="logo" />
        <!-- TODO: заменить на роутер линк когда будет роутер -->
        <p v-for="({ title, link }) in links" :key="link + title" class="header__link">{{ title }}</p>
    </div>
    <div>
        <Button class="header__first-btn">Войти</Button>
        <Button :style="'outlined'">Регистрация</Button>
    </div>
  </div>
</template>

<script setup>
//components
import Button from "../buttons/Button.vue"
//images
import Logo from "../../assets/images/logo.svg";


//state
const links = [
    {
        title: 'Доставка',
        link: '#'
    },
    {
        title: 'Оплата',
        link: '#'
    },
    {
        title: 'Контакты',
        link: '#'
    },
]
</script>

<style scoped>
.header {
  width: 100%;
  height: 80px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding-left: 24px;
  background: #ffffff;
  border-bottom: 1px solid #f0f0f0;
}

.header div {
    padding-right: 30px;
    display: flex;
}

.header__link {
  margin-left: 48px;
  cursor: pointer;
  font-family: "Montserrat";
  font-style: normal;
  font-weight: 400;
  font-size: 25px;
  line-height: 30px;
  color: #333333;
}

.header__first-btn {
    margin-right: 12px;
}
</style>