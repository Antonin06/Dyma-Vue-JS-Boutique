<script setup lang="ts">
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Cart from "@/components/Cart/Cart.vue";
import Shop from "@/components/Shop/Shop.vue";
import data from '@/data/product';
import {reactive} from "vue";

import type {ProductInterface} from "@/interfaces/product.interface";

const state = reactive<{
  products: ProductInterface[],
  cart: ProductInterface[]
}>({
  products: data,
  cart: []
});

function addProductToCart(productID: number) {
  const product = state.products.find((product) => product.id === productID);
  if(product && !state.cart.find((product) => product.id === productID)) {
    state.cart.push({ ...product });
  }
}

console.log(state.products)
</script>

<template>
  <div class="app-container">
    <Header class="header"/>
    <Shop :products="state.products" @add-product-to-cart="addProductToCart" class="shop"/>
    <Cart class="cart"/>
    <Footer class="footer"/>
  </div>
</template>

<style lang="scss">
@import "./assets/base.scss";
</style>
