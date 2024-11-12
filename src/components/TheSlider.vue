<template>
  <div class="mt-8">
  <div class="flex justify-between" >
    
  <button @click="prevImg" class="h-10 w-10 mt-16 rounded-full border-black border-2 border-solid"> &lt; </button>

  <img :src="images[currentIndex].src" alt="image"/>

  <button @click="nextImg" class="h-10 w-10 mt-16 rounded-full border-black border-2 border-solid"> &gt; </button>
  </div>

  </div>
</template>

<script lang="ts">
export default {
  data() {
    return {
      currentIndex:1,
      images: [{
        src: "/images/1.jpeg"
      },
      {
        src: "/images/1.jpeg"
      },
      {
        src: "/images/2.jpeg"
      },
      {
        src: "/images/3.jpeg"
      },
      {
        src: "/images/4.jpeg"
      },
      {
        src: "/images/5.jpeg"
      },
    ]
    }
  },
  methods:{
    nextImg()
    {
      if(this.currentIndex === this.images.length )
    {
      this.currentIndex=0;
    }
    else {
      this.currentIndex++;
    }


    },
    prevImg()
    {
      if(this.currentIndex === 0 )
    {
      this.currentIndex=this.images.length;
    }
    else {
      this.currentIndex--;
    }
    },

  }
}
</script>

<style scoped>
/* You can add any additional styles here if needed */
</style>
