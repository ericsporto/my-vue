<script lang="ts">
import AppProduct from './AppProduct.vue';

export default {
  components: {
    AppProduct,
  },
};
</script>

<template>
  <div class="flex flex-col my-10">
    <div class="space-y-10">
      <div>
        <h1>Produtos</h1>
      </div>
      <div>
        <AppProduct
          v-for="product in $store.state.products"
          :key="product.id"
          :product="product"
        />
      </div>
    </div>
  </div>
</template>
