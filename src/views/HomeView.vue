

<template>
  <main  class="mt-64 w-screen">
    <h1 class="text-center">home</h1>
    <TheSlider/>
  </main>
</template>


<script lang="ts">
import TheSlider from '@/components/TheSlider.vue';
export default {
  data() {
    return {
      
    }
  },
  components:{
    TheSlider,
  }
}
</script>

<style scoped>
  main{
    /* width: 100%;
    max-width: 100vw; */
    overflow-x: hidden; /* Prevent horizontal scrolling */
  }

</style>
