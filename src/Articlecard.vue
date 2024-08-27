<script setup>
const props = defineProps({
  article: {
    type: Object,
    required: true
  },
  index: {
    type: Number
  }
})
</script>

<template>
  <div class="card">
    <img :src="article.image" :alt="article.title" />
    <div class="card-description">
      <div class="card-category">
        <h2 class="h2-gradient">{{ article.category }}</h2>
        <h2>{{ article.subCategory }}</h2>
      </div>

      <p class="article-text">{{ article.title }}</p>

      <p class="article-date">{{ article.date }}</p>
    </div>
  </div>
</template>

<style scoped>
.card {
  height: 480px;
  width: calc((100% - 90px) / 4);
  /* border: solid red 1px; */
}

img {
  width: 100%;
  height: 75%;
  object-fit: cover;
}

.card-category {
  display: flex;
  gap: 10px;
  margin-top: 10px;
}

.article-text {
  font-family: 'Merriweather';
  font-size: 14px;
  font-weight: bold;
  line-height: 18px;
  margin-top: 10px;
}

.article-date {
  font-size: 12px;
  margin-top: 10px;
}
</style>
