<template>
  <div class="slideshow-container">

    <!-- Full-width images with number and caption text -->
    <div class="mySlides fade">
      <div class="numbertext">{{ currentIndex+1 }} / {{ images.length }}</div>
      <img :src="images[currentIndex].src" style="width:100%; height: 500px;"  />
      <div class="text">Caption Text</div>
    </div>

    <!-- Next and previous buttons -->
    <a @click="prevImg" class="prev">&#10094;</a>
    <a @click="nextImg" class="next">&#10095;</a>
  </div>
  <br>

  <!-- The dots/circles -->
  <div  style="text-align:center">
    <span @click="changeCurrentIndex(index)" :class="index===currentIndex? 'active':''" v-for="(image, index) in images" :key="index" class="dot"></span>
  </div>


</template>

<script lang="ts">
export default {
  data() {
    return {
      currentIndex: 0,
      images: [{
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
  methods: {
    nextImg() {
      if (this.currentIndex === this.images.length-1) {
        this.currentIndex = 0;
      }
      else {
        this.currentIndex++;
      }


    },
    prevImg() {
      if (this.currentIndex === 0) {
        this.currentIndex = this.images.length;
      }
      else {
        this.currentIndex--;
      }
    },
    changeCurrentIndex(index:number) {
      this.currentIndex = index;

    }

  }
}
</script>

<style scoped>
.slideshow-container {
  max-width: 1000px;
  position: relative;
  margin: 20px auto;
}


.prev,
.next {
  cursor: pointer;
  position: absolute;
  top: 50%;
  width: auto;
  margin-top: -22px;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.6s ease;
  border-radius: 0 3px 3px 0;
  user-select: none;
}

.next {
  right: 0;
  border-radius: 3px 0 0 3px;
}

.prev:hover,
.next:hover {
  background-color: rgba(0, 0, 0, 0.8);
}

.text {
  color: #f2f2f2;
  font-size: 15px;
  padding: 8px 12px;
  position: absolute;
  bottom: 8px;
  width: 100%;
  text-align: center;
}

.numbertext {
  color: #f2f2f2;
  font-size: 12px;
  padding: 8px 12px;
  position: absolute;
  top: 0;
}

.dot {
  cursor: pointer;
  height: 15px;
  width: 15px;
  margin: 0 2px;
  background-color: #bbb;
  border-radius: 50%;
  display: inline-block;
  transition: background-color 0.6s ease;
}

.active,
.dot:hover {
  background-color: #717171;
}
</style>
