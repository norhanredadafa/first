<script setup lang="ts">
import { RouterView } from 'vue-router'
import headerComp from './components/TheHeader.vue'
</script>

<template>
  <div>
    <headerComp />

    <RouterView />
  </div>
</template>

<style scoped></style>
