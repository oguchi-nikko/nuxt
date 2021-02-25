<template>
  <div>
    <h2>関連リンク</h2>
    <div class="flex-topic-box">
      <div v-for="item in items" :key="item.title" class="flex-topic-item">
        <a :href="item.url" target="_blank"><img :src="item.picture" /></a>
        <div>{{ item.title }}</div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      items: [
        {
          url: 'http://o-guchi.yokohama/',
          picture: require('@/assets/shopping_street.jpg'),
          title: 'おおぐち通商店街',
        },
        {
          url: 'https://kunpuu.base.shop/',
          picture: require('@/assets/teacup.jpg'),
          title: '姉妹店 Kunpuu',
        },
        {
          url: 'https://note.com/oguchi_nikko',
          picture: require('@/assets/royal_copenhagen.JPG'),
          title: '日光陶器 note',
        },
      ],
    }
  },
}
</script>
<style scoped>
.flex-topic-box {
  display: flex;
  justify-content: space-between;
}
.flex-topic-item {
  background: #fbfaf5;
  box-shadow: 0 1rem 2rem hsl(0 0% 0% / 8%);
  display: inline-block;
  margin-right: 1em;
  padding: 3% 3% 5% 3%;
  width: calc(100% / 3);
}
.flex-topic-item div {
  font-size: 1vw;
  margin-top: 1.5em;
}
</style>
