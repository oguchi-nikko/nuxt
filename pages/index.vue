<template>
  <div class="container text-center">
    <Header />
    <Swiper />
    <div class="w-4/5 mx-auto">
      <About />
      <Recommend />
      <OtherInfo />
    </div>
    <PageTop />
    <Footer />
  </div>
</template>

<script>
import Header from '@/components/Header.vue'
import Swiper from '@/components/Swiper.vue'
import About from '@/components/About.vue'
import OtherInfo from '@/components/OtherInfo.vue'
import Recommend from '@/components/Recommend.vue'
import PageTop from '@/components/PageTop.vue'
import Footer from '@/components/Footer.vue'
export default {
  components: {
    Header,
    Swiper,
    About,
    Recommend,
    OtherInfo,
    PageTop,
    Footer,
  },
  computed: {
    windowSize() {
      return window.innerWidth
    },
  },
}
</script>

<style>
.container {
  margin: auto;
  align-items: center;
}
</style>
