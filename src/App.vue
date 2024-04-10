
<template>
  <ButtonSizeBackground ref="btnBg"></ButtonSizeBackground>
</template>

<script setup>
import ButtonSizeBackground from "@/components/ButtonSizeBackground.vue";
import {onMounted, ref} from "vue";
const btnBg =  ref()
console.log(btnBg.value)
</script>

<style scoped>

</style>