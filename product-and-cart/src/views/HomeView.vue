<template>
  <div class="home">
    <div class="splash-container">
      <div class="splash">
        <h1>Splendid Food</h1>
      </div>
    </div>

    <main class="wrapper">
      <h2>Recommended</h2>

      <div class="recommended">

        <ProductCard
          v-for="(product, index) in inventory.slice(0, 3)"
          :key="product.id"
          class="card"
          :index="index"
          :product="product"
          :addToCart="addToCart"
        />

      </div>
    </main>
  </div>
</template>

<script>
// import food from '../food.json'
import ProductCard from '@/components/ProductCard.vue'

export default {
  name: 'HomeView',
  // data () {
  //   return {
  //     inventory: food
  //   }
  // },
  props: ['inventory', 'addToCart'],
  // props: ['addToCart'],
  components: {
    ProductCard
  },
  mounted () {
    // console.log(food)
  }
}
</script>
