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
        <h1>
          <span>{{ data.frontPage.title }}</span>
        </h1>
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
  margin: 70px auto;
  background-image: v-bind("`url('${data.frontPage.image}')`");
  background-position: bottom;
  background-size: cover;
  padding: 90px;
}

/* -- TOP FRONT PAGE ----------*/
.top-main-block {
  position: relative;
}

.bar-absolute {
  height: 101.5%;
  width: 5px;
  background: linear-gradient(180deg, rgba(190, 128, 255, 1) 0%, rgba(99, 37, 255, 1) 100%);
  position: absolute;
}

.top-text-block {
  margin-left: 5px;
}

.top-category {
  display: flex;
  background-color: black;
  gap: 15px;
  padding: 5px;
  width: 170px;
}

h2 {
  color: white;
}

h1 {
  color: white;
  width: 67%;
}

h1 > span {
  background-color: black;
  line-height: 45px;
  padding: 7px;
}

/* -- DESCRIPTION ----------*/
.description-block {
  margin-top: 50px;
  padding: 30px;
  background-color: rgba(0, 0, 0, 0.7);
  width: 80%;
}

.description-block > p {
  color: white;
  font-size: 14px;
  font-weight: 300;
  line-height: 25px;
  letter-spacing: 1px;
}
</style>
