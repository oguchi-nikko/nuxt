<template>
  <div>
    <h2>おすすめトピックス</h2>
    <div class="flex-topic-box">
      <div v-for="item in items" :key="item.title" class="flex-topic-item">
        <a @click="$router.push(item.url)"><img :src="item.picture" /></a>
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
          url: '/particularAbout',
          picture: require('@/assets/nikkochina.jpg'),
          title: '当店のこだわり',
        },
        {
          url: '/enjoy',
          picture: require('@/assets/baby_on_dishes.jpg'),
          title: '楽しみ方',
        },
        {
          url: '/inside',
          picture: require('@/assets/girl_on_dishes.jpg'),
          title: '店内の様子',
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
