<script lang="ts">
export default {
  data(){
    return {

    }
  }, 
};
</script>

<template>
  <div
    class="flex flex-col w-full justify-center items-center h-full space-y-10"
  >
    <nav>
      <router-link to="/">Home</router-link>
      <router-link to="/about">About</router-link>
    </nav>
    <router-view />
  </div>
</template>
