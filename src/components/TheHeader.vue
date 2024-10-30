<template>
  <div class="fixed top-0 left-0 w-full bg-white shadow">
    <header class="flex justify-between items-center p-4">
      <div class="flex-shrink-0">
        <img src="../assets/images/Untitled.jpeg" width="100" height="100" alt="logo" />
      </div>
      <nav class="flex-grow text-center">
        <RouterLink to="/" class="mx-4">Home</RouterLink>
        <RouterLink to="/about" class="mx-4">About</RouterLink>
      </nav>
      <div class="flex space-x-4">
        <button class="py-2 px-4 bg-blue-500 text-white rounded">Switch Language</button>
        <button class="py-2 px-4 bg-green-500 text-white rounded">Sign Up</button>
      </div>
    </header>
  </div>
</template>

<script lang="ts">
import { RouterLink } from 'vue-router';

export default {
  components: {
    RouterLink
  }
}
</script>

<style scoped>
/* You can add any additional styles here if needed */
</style>
