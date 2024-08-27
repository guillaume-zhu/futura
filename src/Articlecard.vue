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
        <h2 class="h2-gradient">{{ article.subCategory }}</h2>
      </div>

      <p>{{ article.title }}</p>

      <p>{{ article.date }}</p>
    </div>
  </div>
</template>

<style scoped>
.card {
  height: 480px;
  width: calc((100% - 90px) / 4);
  border: solid red 1px;
}
img {
  width: 50px;
}
</style>
