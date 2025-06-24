<script setup>
const props = defineProps({
  articleCard: {
    type: Array,
    required: true,
  },
})
</script>

<template>
  <div class="container">
    <article v-for="article in articleCard" :key="article.id">
      <img :src="article.image" :alt="article.title" />
      <div class="meta">
        <a href="" class="roboto-300 category">{{ article.category }}</a>
        <a href="" class="roboto-300 subCategory">{{ article.subCategory }}</a>
      </div>
      <h3 class="merriweather-700">{{ article.title }}</h3>
      <p class="roboto-300">{{ article.date }}</p>
    </article>
  </div>
</template>

<style scoped>
.container {
  width: 1300px;
  max-width: 90%;
  margin: 60px auto;

  display: grid;
  grid-template-columns: 1fr 1fr 1fr 1fr;
  grid-gap: 30px;
}
article {
  width: 100%;
}
article > img {
  width: 100%;
  height: 300px;
  object-fit: cover;
}
.meta {
  background-color: transparent;
  margin-top: 8px;
}
.meta > a.subCategory {
  color: black;
}
h3,
p {
  padding: 4px;
}
h3 {
  font-size: 14px;
  line-height: normal;
}
p {
  color: gray;
  font-size: 12px;
}
</style>
