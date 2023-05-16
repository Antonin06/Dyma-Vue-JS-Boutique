<script setup lang="ts">
import ShopProduct from "@/components/Shop/ShopProduct.vue";
</script>

<template>
	<div class="grid">
		<ShopProduct />
		<ShopProduct />
		<ShopProduct />
		<ShopProduct />
		<ShopProduct />
		<ShopProduct />
	</div>
</template>

<style scoped lang="scss">
.grid {
	display: grid;
	grid-template-columns: repeat(3, 1fr);
	grid-gap: 1rem;
}
</style>