<template>
  <div class="swiper-container relative">
    <hooper
      :progress="true"
      :auto-play="true"
      :play-speed="5000"
      :transition="1000"
      style="height: 100%"
    >
      <slide><img src="..\assets\hooper\ricebowls.jpg" /></slide>
      <slide><img src="..\assets\hooper\paprika.jpg" /></slide>
      <slide><img src="..\assets\hooper\daruma.jpg" /></slide>
      <slide><img src="..\assets\hooper\fish.jpg" /></slide>
      <slide><img src="..\assets\hooper\pot.jpg" /></slide>
    </hooper>
  </div>
</template>

<script>
import { Hooper, Slide } from 'hooper'
import 'hooper/dist/hooper.css'
export default {
  components: {
    Hooper,
    Slide,
  },
}
</script>
<style scoped>
.swiper-container {
  /* 最背面にしたい時、z-index:-1 & relativeに設定 */
  z-index: -1;
}
</style>
