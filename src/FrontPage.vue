<script setup>
const props = defineProps({
  data: {
    type: Object,
    required: true
  }
})
</script>

<template>
  <section class="container">
    <div class="top-main-block">
      <div class="bar-absolute"></div>

      <div class="top-text-block">
        <div class="top-category">
          <h2 class="h2-gradient">{{ data.frontPage.category }}</h2>
          <h2>{{ data.frontPage.subCategory }}</h2>
        </div>
        <h1>{{ data.frontPage.title }}</h1>
      </div>
    </div>

    <div class="description-block">
      <p>{{ data.frontPage.teaser }}</p>
    </div>
  </section>
</template>

<style scoped>
section {
  height: 550px;
  border: 1px solid salmon;
  margin: 0 auto;
  background-image: v-bind("`url('${data.frontPage.image}')`");
  background-position: bottom;
  background-size: cover;
}
</style>
