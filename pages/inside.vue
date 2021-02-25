<template>
  <div class="container text-center">
    <Header />
    <div class="w-4/5 mx-auto">
      <h2>店内の様子</h2>
      <video
        src="@/assets/inside_store.mp4"
        controls
        controlsList="nodownload"
        class="mt-1 mb-2"
      />
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
  data() {
    return {
      items: [
        {
          name: '掘り出し物を見つけよう',
          picture: require('@/assets/enjoy01.jpg'),
          sentence:
            '店頭には、常時"お買い得コーナー"が設置されています。\n店主の気分で品揃えが変わるので、あなたの逸品に出会えたらラッキー。',
        },
        {
          name: '季節に合わせたディスプレイを楽しんで',
          picture: require('@/assets/enjoy02.jpg'),
          sentence:
            '春はお雛様。夏は風鈴。秋はお月見。冬は正月飾り。\n当店では、四季を感じる雑貨も取り扱っています！\n\n今年の夏は、ハワイアンコーナーが好評でした♪',
        },
        {
          name: '年2回の大売出しは絶対お得',
          picture: require('@/assets/enjoy03.jpg'),
          sentence:
            '年に2回開催される大売出しは、超お買い得な"全品3割引き"\nこのチャンスをお見逃しなく！',
        },
      ],
    }
  },
}
</script>
<style>
.container {
  margin: auto;
  align-items: center;
}
.enjoy-content p {
  margin-top: 3.5em;
}
</style>
