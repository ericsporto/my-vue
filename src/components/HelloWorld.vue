<script lang="ts">
export default {
  props: ['msg'],
  methods: {
    updateUser() {
      const newUser = {
        first_name: 'Val',
        last_name: 'Gonzaga',
        email: 'val_gonzaga@gmail.com',
      };
      this.$store.commit('storeUser', newUser);
    },
  },
  created() {
    this.$store.state.user;
  },
};
</script>

<template>
  <div class="flex justify-center">
    <div class="flex flex-col space-y-6">
      <h1>{{ msg }}</h1>
      <button
        class="bg-red-600 rounded-lg px-4 py-2 gap-5"
        @click="updateUser()"
      >
        Atualizar Usuário
      </button>
      <div class="flex flex-col justify-center items-center">
        <p>{{ $store.state.user.first_name }}</p>
        <p>{{ $store.state.user.last_name }}</p>
        <p>{{ $store.state.user.email }}</p>

      </div>
    </div>
  </div>
</template>

<style scoped></style>
