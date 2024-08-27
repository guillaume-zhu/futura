<script setup>
import Header from './Header.vue'
import FrontPage from './FrontPage.vue'
import Articlecard from './Articlecard.vue'
import Footer from './Footer.vue'

import data from './assets/data/articles.json'
</script>

<template>
  <Header />

  <FrontPage v-bind:data="data" />

  <section class="card-section container">
    <Articlecard
      v-for="(article, index) in data.articlesList"
      :key="article.id"
      :article="article"
      :index="index"
    />
  </section>

  <Footer />
</template>

<style scoped>
.card-section {
  /* border: 1px solid purple; */
  display: flex;
  flex-wrap: wrap;
  gap: 30px;
  justify-content: space-between;
}
</style>
