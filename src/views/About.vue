<script lang="ts">
import AppProducts from '../components/Products/AppProducts.vue';

export default {
  components: {
    AppProducts,
  },
};
</script>
<template>
  <div>
    <h1>About</h1>
    <AppProducts />
    <pre>
      <p>{{ $store.state.cart }}</p>
    </pre>
    <pre>
      <p>{{ $store.getters.total }}</p>
    </pre>
  </div>
</template>
