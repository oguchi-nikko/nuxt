<template>
  <div class="container text-center">
    <Header />
    <div class="w-4/5 mx-auto">
      <h2>アクセス</h2>
      <div class="google-map">
        <iframe
          src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d6497.13615559514!2d139.644728!3d35.490229!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x0%3A0xc997b197e78b749d!2z77yI5pyJ77yJ5pel5YWJ6Zm25Zmo!5e0!3m2!1sja!2sjp!4v1614133651024!5m2!1sja!2sjp"
          width="400"
          height="300"
          style="border: 0"
          allowfullscreen=""
          loading="lazy"
        ></iframe>
      </div>
      <ul class="text-left">
        <li class="address">221-0002 神奈川県横浜市神奈川区大口通11-2</li>
        <li class="tel">
          <span class="ml-1"><a href="tel:045-401-8561">045-401-8561</a></span>
        </li>
        <li class="business-hours">
          <span class="ml-1">10:00-19:00 (定休日:木曜)</span>
        </li>
        <li class="access">
          JR横浜線 大口駅西口 徒歩3分 / 京浜急行 子安駅 徒歩10分
        </li>
      </ul>
    </div>
    <PageTop />
    <Footer />
  </div>
</template>
<script>
import Header from '@/components/Header.vue'
import Footer from '@/components/Footer.vue'
import PageTop from '@/components/PageTop.vue'
export default {
  components: {
    Header,
    Footer,
    PageTop,
  },
}
</script>
<style scoped>
.container {
  margin: auto;
  align-items: center;
}
.google-map {
  position: relative;
  width: 100%;
  height: 0;
  padding-top: 75%;
  margin: 2em 0;
}
.google-map iframe {
  position: absolute;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
}
li {
  font-size: 1vw;
  margin-left: 1.5vw;
  margin-bottom: 0.5em;
}

.address::before {
  background: url('../assets/icon/address.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 2.5em;
  margin-right: 0.9em;
  max-height: 16px;
  max-width: 16px;
  position: relative;
  width: 2.5em;
  z-index: -1;
}

.tel::before {
  background: url('../assets/icon/tel.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 2.5em;
  margin-right: 1em;
  max-height: 16px;
  max-width: 16px;
  position: relative;
  width: 2.5em;
  z-index: -1;
}

.business-hours::before {
  background: url('../assets/icon/clock.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 2.5em;
  margin-right: 1em;
  max-height: 16px;
  max-width: 16px;
  position: relative;
  width: 2.5em;
  z-index: -1;
}

.access::before {
  background: url('../assets/icon/train.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 2.5em;
  margin-right: 0.9em;
  max-height: 16px;
  max-width: 16px;
  position: relative;
  width: 2.5em;
  z-index: -1;
}
</style>
