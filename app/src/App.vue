<template>
  <div>
    <h1>Jono Shawarma</h1>

<div class ="container"></div>

<div>This one halal</div>
<img 
  v-for="item in meats" 
  :key="item.name"
  :src="item.img"
  :alt="item.name"
  @click="orderAdd(item.name, item.price)"
/>


  </div>
</template>

<script setup>
const meats = [
        { name: 'Beef', price: 11.99, img: '/beef.jpg' },
        { name: 'Lamb', price: 11.99, img: '/lamb.jpg' },
        { name: 'Chicken', price: 10.99, img: '/chicken.jpg' },
        { name: 'Mutton', price: 10.99, img: '/mutton.jpg' },
        { name: 'Turkey', price: 10.99, img: '/turkey.jpg' }
      ]
const salads = [
        { name: 'Lettuce', price: 1.50, img: '/lettuce.jpg' },
        { name: 'Onions', price: 0.99, img: '/onions.jpg' },
        { name: 'Tomato', price: 1.50, img: '/tomato.jpg' },
        { name: 'Pickle', price: 0.99, img: '/pickle.jpg' },
        { name: 'Peppers', price: 1.25, img: '/peppers.jpg' },
        { name: 'Cucumbers', price: 0.99, img: '/cucumbers.jpg' }
      ]
const sauces = [
        { name: 'Hot Sauce', price: 0.50, img: '/hot.jpg' },
        { name: 'Tahini', price: 0.50, img: '/tahini.jpg' },
        { name: 'Tzatziki', price: 0.50, img: '/tzatziki.jpg' },
        { name: 'White Sauce', price: 0.50, img: '/white.jpg' }
      ],
      sides: [
        { name: 'Dolma', price: 1.50, img: '/dolma.jpg' },
        { name: 'Falafel', price: 1.99, img: '/falafel.jpg' },
        { name: 'Fries', price: 2.99, img: '/fries.jpg' },
        { name: 'White Rice', price: 4.99, img: '/white rice.webp' },
        { name: 'Yellow Rice', price: 5.99, img: '/yellow rice.jpg' }
      ],
      drinks: [
        { name: 'Coke', price: 2.50, img: '/coke.jpg' },
        { name: 'Brisk', price: 2.50, img: '/brisk.jpg' },
        { name: 'Dr.Pepper', price: 2.50, img: '/dr.pepper.jpg' },
        { name: 'Fanta', price: 2.50, img: '/fanta.jpg' },
        { name: 'Ginger Ale', price: 2.50, img: '/ginger ale.jpg' },
        { name: 'Mug', price: 2.50, img: '/mug.jpg' },
        { name: 'Sprite', price: 2.50, img: '/sprite.jpg' }
      ]
    }
  }
}

let meal =[]
let total= 0
function orderAdd(food,price){
  meal.push.food
  total+=price
}


</script>

<style lang="scss" scoped>

</style>