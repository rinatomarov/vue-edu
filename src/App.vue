<template>
  <router-view></router-view>
  <h1>App Vue Application</h1>
  <a href="/">HOME</a>
  <br>
  <a href="/about">ABOUT</a>
  <br>
  <a href="/router">ROUTER</a>
  <br>
  <br>
  <!-- SPA - single page application -->

  <router-link to="/">HOME</router-link>
  <br>
  <router-link to="/about">ABOUT</router-link>
  <br>
  <router-link to="/router">ROUTER</router-link>
  <br>
  <br>

  <button @click="redirect('/')">Go Home</button>
  <button @click="redirect('/router')">Go Router</button>
  <button @click="redirect('/about')">Go About</button>
  <br>
  <br>
<!--<AboutMe></AboutMe>-->
</template>

<script setup>
import AboutMe from "@/views/AboutMe.vue";
import { useRouter } from "vue-router";
const router = useRouter()
const redirect = (path) => {
  console.log(path)
  router.push(path)
  // window.location.href = path
}

</script>
<style scoped>

</style>