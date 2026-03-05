<template>
  <div id="shawarmaPage">
    <h1>Jono Shawarma</h1>
    <p>This one halal</p>

    <div class="jsImages">
      <div v-for="item in orders" :key="item.name" class="itemCard" @click="orderAdd(item)">
        <img :src="item.img" :alt="item.name">
        <div class="itemInfo">
          <h3>{{ item.name }}</h3>
          <p>${{ item.price }}</p>
        </div>
      </div>
    </div>

    <h2>Your Order</h2>
    <ul>
      <li v-for="(o,i) in meal" :key="i">{{ o.name }} - ${{ o.price }}</li>
    </ul>

    <h2>Total: ${{ total }}</h2>
  </div>
</template>

<script setup>
import { ref } from 'vue'

const orders = [
  { name:'Beef',price:11.99,img:'/beef.jpg',category:'meat'},
  { name:'Lamb',price:11.99,img:'/lamb.jpg',category:'meat'},
  { name:'Chicken',price:10.99,img:'/chicken.jpg',category:'meat'},
  { name:'Mutton',price:10.99,img:'/mutton.jpg',category:'meat'},
  { name:'Turkey',price:10.99,img:'/turkey.jpg',category:'meat'},
  { name:'Lettuce',price:1.50,img:'/lettuce.jpg',category:'salad'},
  { name:'Onions',price:.99,img:'/onions.jpg',category:'salad'},
  { name:'Tomato',price:1.50,img:'/tomato.jpg',category:'salad'},
  { name:'Pickle',price:.99,img:'/pickle.jpg',category:'salad'},
  { name:'Peppers',price:1.25,img:'/peppers.jpg',category:'salad'},
  { name:'Cucumbers',price:.99,img:'/cucumbers.jpg',category:'salad'},
  { name:'Hot Sauce',price:.50,img:'/hot.jpg',category:'sauce'},
  { name:'Tahini',price:.50,img:'/tahini.jpg',category:'sauce'},
  { name:'Tzatziki',price:.50,img:'/tzatziki.jpg',category:'sauce'},
  { name:'White Sauce',price:.50,img:'/white.jpg',category:'sauce'},
  { name:'Pita',price:2.99,img:'/pita.jpg',category:'side'},
  { name:'Dolma',price:1.50,img:'/dolma.jpg',category:'side'},
  { name:'Falafel',price:1.99,img:'/falafel.jpg',category:'side'},
  { name:'Fries',price:2.99,img:'/fries.jpg',category:'side'},
  { name:'White Rice',price:4.99,img:'/white rice.webp',category:'side'},
  { name:'Yellow Rice',price:5.99,img:'/yellow rice.jpg',category:'side'},
  { name:'Coke',price:2.50,img:'/coke.jpg',category:'drink'},
  { name:'Brisk',price:2.50,img:'/brisk.jpg',category:'drink'},
  { name:'Dr.Pepper',price:2.50,img:'/dr.pepper.jpg',category:'drink'},
  { name:'Fanta',price:2.50,img:'/fanta.jpg',category:'drink'},
  { name:'Ginger Ale',price:2.50,img:'/ginger ale.jpg',category:'drink'},
  { name:'Mug',price:2.50,img:'/mug.jpg',category:'drink'},
  { name:'Sprite',price:2.50,img:'/sprite.jpg',category:'drink'}
]

const meal = ref([])
const total = ref(0)

function orderAdd(item){
  meal.value.push(item)
  total.value += item.price
}
</script>

<style scoped>
#shawarmaPage{
  display:flex;
  flex-direction:column;
  align-items:center;
  text-align:center;
  border:1px solid #ccc;
  border-radius:10px;
  background:white;
  padding-bottom:20px;
  box-shadow:0 4px 8px rgba(0,0,0,.2);
}

.jsImages{
  width:100%;
  max-width:1000px;
  display:grid;
  grid-template-columns:repeat(4,1fr);
  gap:15px;
}

.itemCard{
  background:white;
  border-radius:10px;
  overflow:hidden;
  box-shadow:0 3px 6px rgba(0,0,0,.15);
  cursor:pointer;
  transition:.15s;
}

.itemCard:hover{
  transform:translateY(-4px);
  box-shadow:0 6px 12px rgba(0,0,0,.25);
}

.itemCard img{
  width:100%;
  height:120px;
  object-fit:cover;
}

.itemInfo{ padding:8px }

.itemInfo h3{ margin:0;font-size:16px }

.itemInfo p{ margin:4px 0 0;font-weight:bold;color:#444 }
</style>