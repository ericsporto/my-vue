<script lang="ts">
export default {
  props: {
    product: Object,
  },
  data() {
    return {
        isInCart: false
    };
  },
  methods: {
    addProduct() {
      this.$store.commit('addProduct', this.product);
    },
    removeProduct() {
      this.$store.commit('removeProduct', this.product.id);
    },
  },

};
</script>
<template>
  <div class="bg-red-500 p-2 rounded mb-2 space-x-2">
    {{ product.name }} - {{ product.price }}
    <button @click="addProduct()" class="bg-blue-800 rounded p-1">
      Adicionar
    </button>
    <button @click="removeProduct()" class="bg-green-800 rounded p-1">
      Remover
    </button>
  </div>
</template>
