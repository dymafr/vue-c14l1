<script setup lang="ts">
import Shop from './components/Shop/Shop.vue';
import Cart from './components/Cart/Cart.vue';
</script>

<template>
  <Shop
    @update-filter="updateFilter"
    :products="filteredProducts"
    :filters="state.filters"
    @add-product-to-cart="addProductToCart"
    class="shop"
  />
  <Cart
    v-if="!cartEmpty"
    :cart="state.cart"
    class="cart"
    @remove-product-from-cart="removeProductFromCart"
  />
</template>

<style lang="scss"></style>
