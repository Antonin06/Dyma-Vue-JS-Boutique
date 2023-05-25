<script setup lang="ts">
  import ShopProductList from "@/components/Shop/ShopProductList.vue";
  import type {ProductInterface} from "@/interfaces/product.interface";

  defineProps<{
    products: ProductInterface[]
  }>()

  const emit = defineEmits<{
    (e: 'addProductToCart', productID: number): void
  }>()
</script>

<template>
<div>
    <ShopProductList
        :products="products"
        @add-product-to-cart="emit('addProductToCart', $event)"
    />
</div>
</template>

<style scoped lang="scss">

</style>