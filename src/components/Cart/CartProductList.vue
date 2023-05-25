<script setup lang="ts">
import CartProduct from "@/components/Cart/CartProduct.vue";
</script>

<template>
	<div class="grid">
		<CartProduct />
		<CartProduct />
		<CartProduct />
	</div>
</template>

<style scoped lang="scss">
  .grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    grid-gap: 1rem;
  }
</style>