<script setup lang="ts">
import type { Product } from "~/types";

defineProps<{
  products: Product[];
}>();
</script>

<template>
  <div>
    <h2>Product List</h2>
    <ul>
      <li v-for="product in products" :key="product.id">
        {{ product.name }} - ${{ product.price }}
        <p>{{ product.description }}</p>
      </li>
    </ul>
  </div>
</template>
