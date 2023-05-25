<script setup lang="ts">
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Cart from "@/components/Cart/Cart.vue";
import Shop from "@/components/Shop/Shop.vue";
import data from '@/data/product';
import {reactive} from "vue";
import type {ProductInterface} from "@/interfaces/product.interface";

const products = reactive<ProductInterface[]>(data);
console.log(products)
</script>

<template>
	<div class="app-container">
		<Header class="header"/>
		<Shop :products="products" class="shop"/>
		<Cart class="cart"/>
		<Footer class="footer"/>
	</div>
</template>

<style lang="scss">
@import "./assets/base.scss";
</style>
