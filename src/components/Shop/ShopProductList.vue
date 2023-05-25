<script setup lang="ts">
import ShopProduct from "@/components/Shop/ShopProduct.vue";
import type {ProductInterface} from "@/interfaces/product.interface";

defineProps<{
  products: ProductInterface[]
}>()
</script>

<template>
	<div class="grid">
		<ShopProduct v-for="product of products" :product="product"/>
	</div>
</template>

<style scoped lang="scss">
.grid {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-gap: 1rem;
}
</style>