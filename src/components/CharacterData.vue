<template>
  <table border="1">
    <ul v-for="row in items">
      <li v-for="(col, field) in row">
        {{col}}
      </li>
    </ul>
  </table>
</template>
<script setup>
import Table from "@/components/Table.vue";

defineProps({
  items: Array
})
</script>
<style scoped>
ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}
</style>