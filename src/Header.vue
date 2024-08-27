<script setup></script>

<template>
  <header>
    <img src="./assets/img/logo-futura-dark.svg" alt="futura-logo" />

    <div class="header-category">
      <div>
        <p>SCIENCES</p>
        <font-awesome-icon :icon="['fas', 'chevron-down']" />
      </div>

      <div>
        <p>SANTE</p>
        <font-awesome-icon :icon="['fas', 'chevron-down']" />
      </div>

      <div>
        <p>TECH</p>
        <font-awesome-icon :icon="['fas', 'chevron-down']" />
      </div>

      <div>
        <p>MAISON</p>
        <font-awesome-icon :icon="['fas', 'chevron-down']" />
      </div>

      <div>
        <p>PLANETE</p>
        <font-awesome-icon :icon="['fas', 'chevron-down']" />
      </div>
    </div>

    <button>JE M'ABONNE</button>
  </header>
</template>

<style scoped>
header {
  background: linear-gradient(45deg, rgba(190, 128, 255, 1) 0%, rgba(99, 37, 255, 1) 100%);
  height: 60px;
  display: flex;
  justify-content: space-between;
  padding: 15px 60px;
}

.header-category {
  display: flex;
  justify-content: center;
  align-items: center;
  gap: 20px;
}

.header-category > div {
  display: flex;
}

.header-category p {
  color: white;
  font-size: 14px;
}

svg {
  color: white;
  margin-left: 5px;
  font-size: 12px;
  text-align: center;
  padding-top: 2px;
}

button {
  background-color: #ffaf16;
  border: none;
  color: white;
  padding: 5px 10px;
}
</style>
