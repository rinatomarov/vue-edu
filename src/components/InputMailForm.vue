<template>
  <div class="form">
    <input type="text" :value="inputValue" @input="inputValue = $event.target.value">
    <FirstDemo text="Отправить"></FirstDemo>
    <span></span>
  </div>
</template>

<script setup>
import { computed } from "vue";
import FirstDemo from "@/components/FirstDemo.vue";
const props = defineProps({
  value: String
})

</script>

<style scoped>
.form{
  display: flex;
  border: 1px solid #282828;
  max-width: fit-content;
  margin: 40px;
  padding: 20px;
  border-radius: 12px;
  gap: 20px;
}
</style>