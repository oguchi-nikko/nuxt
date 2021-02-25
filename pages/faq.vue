<template>
  <div class="container text-center">
    <Header />
    <div class="w-4/5 mx-auto">
      <h2>Q＆A</h2>
      <details v-for="item in items" :key="item.question">
        <summary class="p-3">{{ item.question }}</summary>
        <p class="whitespace-pre-line" v-text="item.answer"></p>
      </details>
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
          question: '支払方法には、どんな種類がありますか？',
          answer: '当店の取り扱いは、現金のみとなっております。',
        },
        {
          question: '最新情報を入手するには？',
          answer: '当店の公式Instagramをご覧ください。',
        },
        {
          question: 'ラッピングサービスは行っていますか？',
          answer: '',
        },
        {
          question: '店舗への連絡方法を教えてください。',
          answer:
            '電話もしくはメールにてお問い合わせください。\n電話番号 : 045-401-8561\nメールアドレス : oguchi.nikko@gmail.com',
        },
        {
          question: '公式SNS掲載の商品が欲しい。',
          answer:
            '商品の在庫を確認した上での取り置きは可能です。\n遠方でご来店が難しい場合は、要相談可能です。お問い合わせください。',
        },
        {
          question: 'セールは開催していますか？',
          answer:
            '年に2回決算セールを開催しております。\n一部商品を除き、全品3割引きで販売しております。\nなお開催日時に関しましては、公式SNSにてご確認ください。',
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
details {
  font-size: 1vw;
  text-align: left;
  transition: 0.5s;
}
</style>
