<script setup>
const props = defineProps({
  articleFrontPage: {
    type: Object,
    required: true, // 👈 Props déclarer comme indispensable
  },
})
</script>

<template>
  <div class="container">
    <section :style="{ backgroundImage: 'url(' + articleFrontPage.image + ')' }">
      <header>
        <div class="meta">
          <a href="" class="roboto-300 category">{{ articleFrontPage.category }}</a>
          <a href="" class="roboto-300 subCategory">{{ articleFrontPage.subCategory }}</a>
        </div>
        <h1 class="merriweather-700">{{ articleFrontPage.title }}</h1>
      </header>
      <div>
        <p class="roboto-300">{{ articleFrontPage.teaser }}</p>
      </div>
    </section>
  </div>
</template>

<style scoped>
section {
  width: 1300px;
  max-width: 90%;
  margin: 60px auto;
  height: 550px;

  color: white;

  box-sizing: border-box;
  padding: 50px;

  background-size: auto;
  background-position: bottom;

  display: flex;
  flex-direction: column;
  gap: 50px;
}
section > header {
  max-width: 60%;
  border-left: 4px solid #6325ff;
}
section > div {
  max-width: 70%;
}

h1 {
  background-color: black;
  width: fit-content;
  padding: 4px;
  font-size: 28px;
  line-height: normal;
}

p {
  background-color: rgba(0, 0, 0, 0.4);
  padding: 25px;
  font-size: 14px;
  line-height: 1.5em;
}
</style>
