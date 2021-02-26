<template>
  <h1>Photoalbum</h1>
  <img :src="src[currentSrc]" width=400 height=400><br>
  <button @click="backImage" class="arrow">Back image</button>
  <button @click="showImage" class="arrow">Show image</button>
</template>

<script>
//import axios from 'axios'
export default {
  data() {
    return {
      src:["https://pngicon.ru/file/uploads/vinni-pukh-v-png-256x256.png",
      "https://pngimg.com/uploads/minions/minions_PNG17.png",
      "https://demiart.ru/forum/uploads20/post-2976419-1518341512-5a800d882fcc2.png",
      "https://www.pngkey.com/png/full/4-48217_mario-png.png",
      "https://i.stack.imgur.com/ILTQq.png"],
      currentSrc:0
    }
  },
  methods: {
    showImage() {
      if (this.currentSrc<this.src.length-1) {
        this.currentSrc++
      } else {
        this.currentSrc=length(this.src)
      }
    },
    backImage() {
      if (this.currentSrc>0) {
        this.currentSrc--
      } else {
        this.currentSrc=0
      }
    }
  }
}
</script>


<style>
body {
  background-color:red;
}
.arrow {
  margin:10px;
  border:1px solid black;
  font-size:25px;
  font-family:Times New Romain
}
button:hover {
  background-color:#A52A2A;
}
</style>
