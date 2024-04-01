<template>
  <table border="1">
    <tr v-for="row in items">
      <td v-for="(col, field) in row">
        {{ col }}
        <slot :cell="col"></slot>
        <slot :name="field" :cell="col" :row="row"></slot>
      </td>
    </tr>
  </table>
</template>

<script setup>
defineProps({
  items: Array
})
</script>