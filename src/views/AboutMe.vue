
<template>
<h1>It's my Page . Hello ,my dear friend!</h1>
  <button @click="redirect('/')">Go Home</button>
</template>
<script setup>
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