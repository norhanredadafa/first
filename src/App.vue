<script setup lang="ts">
import { RouterView } from 'vue-router'
import headerComp from './components/TheHeader.vue'
</script>

<template>
 
    <headerComp />

    <RouterView />

</template>

<style >
*{
  padding: 0;
  margin: 0;
}

</style>
