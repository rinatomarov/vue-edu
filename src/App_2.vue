<template>
  <CharacterData :items="characterData">
    <template #price="{ cell }">
<!--      <span :style="`color: ${priceColor(cell)}`">-->
<!--        {{ cell }}-->
<!--      </span>-->
    </template>

    <template #default="{ cell }">
<!--      <p>default slot - {{ cell }}</p>-->
    </template>
  </CharacterData>

</template>

<script setup>
import {ref, watch} from "vue";
import Table from "@/components/Table.vue";
import CharacterData from "@/components/CharacterData.vue";
import AddCards from "@/components/AddCards.vue";
const priceColor = (price) => {
  if(price < 2001) return 'green'
  else if(price < 5001) return 'yellow'

  return  'red'
}

const items = [
  {
    name: 'Imac',
    price: 2000,
    description: 'Desktop'
  },
  {
    name: 'MacBook',
    price: 3000,
    description: 'Laptop'
  },
  {
    name: 'Iphone',
    price: 7000,
    description: 'Phone'
  },
]

const characterData = [
  {
    image:'https://cdn-bgp.bluestacks.com/BGP/ru/gametiles_com.mojang.minecraftpe.jpg',
    name:'John Johns',
    profession:'Frontend dev'
  },
  {
    image:'https://awsimages.detik.net.id/community/media/visual/2024/02/12/satoru-gojo-dalam-jujutsu-kaisen_43.jpeg?w=1200',
    name:'Satoru Gojo',
    profession:'Strongest'
  },
  {
    image:'https://sputnik.kz/img/214/27/2142759_385:0:1025:704_1920x0_80_0_0_763ba982862caa49edc9d57d10eef2f2.jpg',
    name:'Kairat Nurtas',
    profession:'Kazakh Singer'
  }
]
</script>