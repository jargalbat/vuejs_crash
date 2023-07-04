<template>
  <header class="top-bar spread">
    <nav class="top-bar-nav">
      <router-link to="/" class="top-bar-link">
        <i class="icofont-spoon-and-fork"></i>
        <span>Home</span>
      </router-link>
      <router-link to="/products" class="top-bar-link">
        <span>Products</span>
      </router-link>
      <router-link to="/past-orders" class="top-bar-link">
        <span>Past Orders</span>
      </router-link>
    </nav>
    <!--    <router-link @click="toggleSidebar" class="top-bar-cart-link">-->
    <!--      <i class="icofont-cart-alt icofont-1x"></i>-->
    <!--      <span>Cart ({{ totalQuantity }})</span>-->
    <!--    </router-link>-->
  </header>

  <router-view/>

  <Sidebar
    v-if="showSidebar"
    :toggle="toggleSidebar"
    :cart="cart"
    :inventory="inventory"
    :remove="removeItem"
  />
</template>

<script setup>
import Sidebar from '@/components/Sidebar.vue'

export default {
  data () {
    return {}
  }
}
// import Sidebar from '@/components/Sidebar.vue'
// import { defineComponent } from 'vue'
//
// export default defineComponent({
//   data () {
//     return {
//       Sidebar
//     }
//   }
// })

</script>
