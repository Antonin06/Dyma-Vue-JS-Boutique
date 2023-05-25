<script setup lang="ts">
  import ShopProductList from "@/components/Shop/ShopProductList.vue";
  import type {ProductInterface} from "@/interfaces/product.interface";

  defineProps<{
    products: ProductInterface[]
  }>()
</script>

<template>
<div>
    <ShopProductList :products="products" />
</div>
</template>

<style scoped lang="scss">

</style>