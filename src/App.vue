<template>
  <h1>APP VUE</h1>
  <!--MPA- multi page application -->

  <!--  <a href="/">HOME</a>-->
  <!--  <br>-->
  <!--  <a href="/about">ABOUT</a>-->
  <!--  <br>-->
  <!--  <a href="/router">ROUTER</a>-->
  <!--  <br>-->
  <!--  <br>-->

  <!--  &lt;!&ndash; SPA - single page application &ndash;&gt;-->

    <router-link to="/">HOME</router-link>
    <br>
    <router-link to="/about">ABOUT</router-link>
    <br>
    <router-link to="/router">ROUTER</router-link>
    <br>
    <br>

  <!--  <button @click="redirect('/')">Go Home</button>-->
  <!--  <button @click="redirect('/router')">Go Router</button>-->
  <!--  <button @click="redirect('/about')">Go About</button>-->
  <!--  <br>-->
  <!--  <br>-->

  <!--  <button @click="login">login</button>-->

  <router-view></router-view>
</template>

<script setup>
import { useRouter } from "vue-router";

const router = useRouter()
const redirect = (path) => {
  console.log(path)
  router.push(path)
  // window.location.href = path
}

const login = () => {
  // валидация
  // запрос
  // обработка

  //редирект на главную/личный кабинет
}
</script>