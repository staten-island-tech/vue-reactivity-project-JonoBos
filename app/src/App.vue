<template>
  <div>
    <h1>Jono Shawarma</h1>

<div class ="container"></div>

<div>This one halal</div>

<h2>Meats</h2>
<img @click ="orderAdd('Beef','11.99')" src="/beef.jpg" alt="">
<img @click ="orderAdd('Lamb','11.99')" src="/lamb.jpg" alt="">
<img @click ="orderAdd('Chicken','10.99')" src="/chicken.jpg" alt="">
<img @click ="orderAdd('Mutton','10.99')" src="/mutton.jpg" alt="">
<img @click ="orderAdd('Turkey','10.99')" src="/turkey.jpg" alt="">

<h2>Salad</h2>
<img @click ="orderAdd('Lettuce','1.50')" src="/lettuce.jpg" alt="">
<img @click ="orderAdd('Onions','0.99')" src="/onions.jpg" alt="">
<img @click ="orderAdd('Tomato','1.50')" src="/tomato.jpg" alt="">
<img @click ="orderAdd('Pickle','0.99')" src="/pickle.jpg" alt="">
<img @click ="orderAdd('Peppers','1.25')" src="/peppers.jpg" alt="">
<img @click ="orderAdd('Cucumbers','0.99')" src="/cucumbers.jpg" alt="">

<h2>Sauces</h2>

<img @click ="orderAdd('Hot Sauce','0.50')" src="/hot.jpg" alt="">
<img @click ="orderAdd('Tahini','0.50')" src="/tahini.jpg" alt="">
<img @click ="orderAdd('Tzatziki','0.50')" src="/tzatziki.jpg" alt="">
<img @click ="orderAdd('White Sauce','0.50')" src="/white.jpg" alt="">

<h2>Sides</h2>
<img @click ="orderAdd('Dolma','1.50')" src="/dolma.jpg" alt="">
<img @click ="orderAdd('Falafel','1.99')" src="/falafel.jpg" alt="">
<img @click ="orderAdd('Fries','2.99')" src="/fries.jpg" alt="">
<img @click ="orderAdd('White Rice','4.99')" src="/white rice.webp" alt="">
<img @click ="orderAdd('Yellow Rice','5.99')" src="/yellow rice.jpg" alt="">

<h2>Drinks</h2>
<img @click ="orderAdd('Coke','2.50')" src="/coke.jpg" alt="">
<img @click ="orderAdd('Brisk','2.50')" src="/brisk.jpg" alt="">
<img @click ="orderAdd('Dr.Pepper','2.50')" src="/dr.pepper.jpg" alt="">
<img @click ="orderAdd('Fanta','2.50')" src="/fanta.jpg" alt="">
<img @click ="orderAdd('Ginger Ale','2.50')" src="/ginger ale.jpg" alt="">
<img @click ="orderAdd('Mug','2.50')" src="/mug.jpg" alt="">
<img @click ="orderAdd('Sprite','2.50')" src="/sprite.jpg" alt="">
  </div>
</template>

<script setup>

let meal =[]
let total= 0
function orderAdd(food,price){
  meal.push.food
  total+=price
}


</script>

<style lang="scss" scoped>

</style>