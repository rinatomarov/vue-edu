<template>
  <div class="cardAdd">
    <div class="card" v-for="elem in cardsArray" :key ='elem.name'>
      <h3>{{ elem.name }}</h3>
      <h3>{{ elem.price }}</h3>
      <FirstDemo text="Добавить в корзину" @click="addPrice(elem.price)"></FirstDemo>
    </div>
  </div>
  <div class="cardPrice">
    <span>Итого вышло на сумму {{totalPriceCard}}</span>
  </div>
</template>
<script setup>
import FirstDemo from "@/components/FirstDemo.vue";
import { computed, ref } from "vue";

const cardsArray = ([
  {name: "Iphone 13 Pro Max", price: 456000},
  {name: "Airpods Max", price: 345000},
  {name: "Macbook 14 Max", price: 1230000}
])
let totalPrice = ref([])
//c помо reduce
let cardPrice = ref(0)
const addPrice = (price) => {
  totalPrice.value.push(price)
  console.log(totalPrice)
  // return  totalPrice
}
const totalPriceCard = computed(() => {
  let sum = totalPrice.value.reduce((acc, val) => acc + val, 0)
  return sum
})

</script>

<style scoped>
.cardAdd {
  display: flex;
  gap: 32px;
  justify-content: flex-start;
}
.card {
  display: flex;
  border: 1px solid;
  width: 200px;
  padding: 16px;
  border-radius: 8px;
  flex-direction: column;
  margin: 32px;
}

h3 {
  margin: auto;
  padding-bottom: 8px;
}
.cardPrice span{
  margin:32px;
  font-family: 'EB Garamond', serif;
  font-weight: bolder;
  font-size: 24px;
}

</style>