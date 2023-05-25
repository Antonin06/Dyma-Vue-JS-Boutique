<script setup lang="ts">

  import type {ProductInterface} from "@/interfaces/product.interface";

  defineProps<{
    product: ProductInterface
  }>()
  // console.log(product)
  const emit = defineEmits<{
    (e: 'addProductToCart', productID: number): void
  }>()
</script>

<template>
  <div class="product">
    <img :src="product.image" alt="">
    <div class="title">{{ product.title }}</div>
    <div class="description">{{ product.description }}</div>
    <div class="price">{{ product.price }}</div>
    <div class="quantity">x 1</div>
    <button @click="emit('addProductToCart', product.id)">Add to cart</button>
  </div>
</template>

<style scoped lang="scss">
.product {
  padding: 20px;
  background: var(--gray-1);
}
</style>