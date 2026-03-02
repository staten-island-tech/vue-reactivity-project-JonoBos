<template>
  <div>
    <h1>Jono Shawarma</h1>

<div class ="container"></div>

<div>This one halal</div>
<img 
  v-for="item in orders" 
  :key="item.name"
  :src="item.img"
  :alt="item.name"
  @click="orderAdd(item.name, item.price)"
/>

  <li v-for="order in meal" :key="order.id">
    {{ item.message }}
  </li>

  </div>
</template>

<script setup>
import { ref } from 'vue';

const orders = [
  // Meats
  { name: 'Beef', price: 11.99, img: '/beef.jpg', category: 'meat' },
  { name: 'Lamb', price: 11.99, img: '/lamb.jpg', category: 'meat' },
  { name: 'Chicken', price: 10.99, img: '/chicken.jpg', category: 'meat' },
  { name: 'Mutton', price: 10.99, img: '/mutton.jpg', category: 'meat' },
  { name: 'Turkey', price: 10.99, img: '/turkey.jpg', category: 'meat' },

  // Salads
  { name: 'Lettuce', price: 1.50, img: '/lettuce.jpg', category: 'salad' },
  { name: 'Onions', price: 0.99, img: '/onions.jpg', category: 'salad' },
  { name: 'Tomato', price: 1.50, img: '/tomato.jpg', category: 'salad' },
  { name: 'Pickle', price: 0.99, img: '/pickle.jpg', category: 'salad' },
  { name: 'Peppers', price: 1.25, img: '/peppers.jpg', category: 'salad' },
  { name: 'Cucumbers', price: 0.99, img: '/cucumbers.jpg', category: 'salad' },

  // Sauces
  { name: 'Hot Sauce', price: 0.50, img: '/hot.jpg', category: 'sauce' },
  { name: 'Tahini', price: 0.50, img: '/tahini.jpg', category: 'sauce' },
  { name: 'Tzatziki', price: 0.50, img: '/tzatziki.jpg', category: 'sauce' },
  { name: 'White Sauce', price: 0.50, img: '/white.jpg', category: 'sauce' },

  // Sides
  { name: 'Dolma', price: 1.50, img: '/dolma.jpg', category: 'side' },
  { name: 'Falafel', price: 1.99, img: '/falafel.jpg', category: 'side' },
  { name: 'Fries', price: 2.99, img: '/fries.jpg', category: 'side' },
  { name: 'White Rice', price: 4.99, img: '/white rice.webp', category: 'side' },
  { name: 'Yellow Rice', price: 5.99, img: '/yellow rice.jpg', category: 'side' },

  // Drinks
  { name: 'Coke', price: 2.50, img: '/coke.jpg', category: 'drink' },
  { name: 'Brisk', price: 2.50, img: '/brisk.jpg', category: 'drink' },
  { name: 'Dr.Pepper', price: 2.50, img: '/dr.pepper.jpg', category: 'drink' },
  { name: 'Fanta', price: 2.50, img: '/fanta.jpg', category: 'drink' },
  { name: 'Ginger Ale', price: 2.50, img: '/ginger ale.jpg', category: 'drink' },
  { name: 'Mug', price: 2.50, img: '/mug.jpg', category: 'drink' },
  { name: 'Sprite', price: 2.50, img: '/sprite.jpg', category: 'drink' }
];


let meal = ref([])
let total= 0

function orderAdd(food,price){
  meal.push(food)
  total= total + price
}


</script>

<style lang="scss" scoped>

</style>