<template>
  <div class="container text-center">
    <Header />
    <div class="w-4/5 mx-auto">
      <img src="@/assets/parent_and_child.png" />
      <div
        v-for="item in items"
        :key="item.name"
        class="paticular-about-content"
      >
        <h2>{{ item.name }}</h2>
        <img :src="item.picture" />
        <p class="whitespace-pre-wrap text-left" v-text="item.sentence"></p>
      </div>
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
          name: 'お茶碗',
          picture: require('@/assets/kodawari01.jpg'),
          sentence:
            '日本のソウルフードである"ごはん"。みなさん、何となくお茶碗を選んでいませんか？\n当店では、子ども用茶碗や夫婦茶碗、ダイエット茶碗などバリエーション豊かなお茶碗をご用意しております。\n毎日使うものだからこそ、"お茶碗"は大事。あなたにピッタリなお茶碗が"日光陶器"なら見つかるはず。',
        },
        {
          name: 'すりこぎ',
          picture: require('@/assets/kodawari02.jpg'),
          sentence:
            '大、中、小...すりこぎ１つ取っても、当店では豊富な種類を取り揃えております。\n用途やご家族の人数に合わせて、チョイスするのがオススメ。\n小さいサイズは1人用はもちろん、赤ちゃんの離乳食用にもピッタリですよ！\n',
        },
        {
          name: '土鍋',
          picture: require('@/assets/kodawari03.jpg'),
          sentence:
            '"土鍋 = 冬"だと思っていませんか？\n土鍋は使い勝手の良い万能調理器具なんですよ！\n当店では、大小様々なサイズの土鍋を年間通して販売しております。\n',
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
.paticular-about-content p {
  margin-top: 3.5em;
}
</style>
