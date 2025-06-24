<script setup>
import Header from './components/Header.vue'
import FrontPage from './components/FrontPage.vue'
import ArticleCard from './components/ArticleCard.vue'
import Footer from './components/Footer.vue'

import articles from './assets/data/articles.json'
const articleFrontPage = articles.frontPage
const articleCard = articles.articlesList
</script>

<template>
  <Header />
  <FrontPage :articleFrontPage="articleFrontPage" />
  <ArticleCard :articleCard="articleCard" />
  <Footer />
</template>

<style scoped></style>
