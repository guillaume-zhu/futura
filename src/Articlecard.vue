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

const categoriesColors = {
  sciences: ['#be80ff', '#6325ff'],
  sante: ['#ff6b9f', '#ff4e52'],
  planete: ['#9fcb5c', '#069849'],
  maison: ['#fa9761', '#ff5957'],
  tech: ['#49adfa', '#2a3df7']
}
</script>

<template>
  <div class="card">
    <img :src="article.image" :alt="article.title" />
    <div class="card-description">
      <div class="card-category">
        <h2
          :class="{
            gradientSciences: article.category === 'sciences',
            gradientSante: article.category === 'sante',
            gradientPlanete: article.category === 'planete',
            gradientMaison: article.category === 'maison',
            gradientTech: article.category === 'tech'
          }"
        >
          {{ article.category }}
        </h2>
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

/* --- gradient categories --------- */

.gradientSciences {
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors.sciences[0]') 0%,
    v-bind('categoriesColors.sciences[1]') 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradientSante {
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors.sante[0]') 0%,
    v-bind('categoriesColors.sante[1]') 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradientPlanete {
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors.planete[0]') 0%,
    v-bind('categoriesColors.planete[1]') 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradientMaison {
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors.maison[0]') 0%,
    v-bind('categoriesColors.maison[1]') 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.gradientTech {
  background: linear-gradient(
    45deg,
    v-bind('categoriesColors.tech[0]') 0%,
    v-bind('categoriesColors.tech[1]') 100%
  );
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
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
