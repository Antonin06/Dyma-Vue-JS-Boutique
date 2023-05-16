<script setup lang="ts">
import Header from "@/components/Header.vue";
import Footer from "@/components/Footer.vue";
import Cart from "@/components/Cart/Cart.vue";
import Shop from "@/components/Shop/Shop.vue";
</script>

<template>
	<div class="app-container">
		<Header class="header"/>
		<Shop class="shop"/>
		<Cart class="cart"/>
		<Footer class="footer"/>
	</div>
</template>

<style lang="scss">
@import "./assets/base.scss";
</style>
