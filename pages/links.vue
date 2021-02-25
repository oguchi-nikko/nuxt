<template>
  <div class="container text-center">
    <Header />
    <div class="w-4/5 mx-auto">
      <h2>リンク集</h2>
      <ul class="links text-left">
        <li>
          公式SNSアカウント
          <ul class="link-list">
            <li>
              <a href="https://www.instagram.com/oguchi_nikko/" target="_blank"
                >Instagram「日光陶器 公式アカウント」</a
              >
            </li>
            <li>
              <a href="https://note.com/oguchi_nikko" target="_blank"
                >note「日光陶器 公式アカウント」</a
              >
            </li>
          </ul>
        </li>
        <li>
          商店街・姉妹店
          <ul class="link-list">
            <li>
              <a href="http://o-guchi.yokohama/" target="_blank"
                >おおぐち通商店街</a
              >
            </li>
            <li>
              <a
                href="https://www.instagram.com/kunpuu.toukiten/"
                target="_blank"
                >Instagram「Kunpuu 公式アカウント」</a
              >
            </li>
            <li>
              <a href="https://kunpuu.base.shop/" target="_blank"
                >Base 「Kunpuu オンラインストア」</a
              >
            </li>
          </ul>
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
<style>
.container {
  margin: auto;
  align-items: center;
}
.links {
  font-size: 1vw;
  list-style-type: disc;
  margin-left: 1.75rem;
}

.links ul {
  margin-bottom: 1.75rem;
}

.links li:first-child {
  margin-top: 0.5rem;
}

.link-list li {
  list-style-type: disc;
  margin-left: 1rem;
}

.link-list li::after {
  background: url('../assets/icon/new_window.svg') no-repeat;
  content: '';
  display: inline-block;
  height: 2.5em;
  margin-left: 0.3em;
  max-height: 16px;
  max-width: 16px;
  position: relative;
  width: 2.5em;
}

.link-list a:hover {
  border-bottom: solid 1px #333631;
}
</style>
