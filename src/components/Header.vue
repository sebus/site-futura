<script setup>
const logoUrl = {
  title: 'Futura',
  url: 'https://www.futura-sciences.com/svg/logo-futura-dark.svg',
}
</script>

<template>
  <div class="container">
    <header>
      <img v-bind:src="logoUrl.url" v-bind:alt="logoUrl.title" />
      <nav>
        <a href="#">Sciences <font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
        <a href="#">Santé <font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
        <a href="#">Tech <font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
        <a href="#">Maison <font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
        <a href="#">Planète <font-awesome-icon :icon="['fas', 'chevron-down']" /></a>
      </nav>
      <button>Je m'abonne</button>
    </header>
  </div>
</template>

<style scoped>
.container {
  background: #be80ff;
  background: linear-gradient(90deg, rgba(190, 128, 255, 1) 0%, rgba(99, 37, 255, 1) 100%);
}
header {
  display: flex;
  flex-direction: row;
  justify-content: space-between;
  align-items: center;

  padding: 10px 0;

  width: 1300px;
  max-width: 90%;
  margin: 0 auto;
}
p {
  text-transform: uppercase;
  font-size: 28px;
}
nav {
  display: flex;
  flex-direction: row;
  gap: 16px;
}
nav > a {
  color: white;
  text-decoration: none;
  text-transform: uppercase;
  font-family: 'Roboto', sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings: 'wdth' 100;

  font-size: 14px;

  display: flex;
  flex-direction: row;
  align-items: center;
  gap: 8px;
}
nav > a > svg {
  font-size: 10px;
}
button {
  background-color: orange;
  padding: 10px 20px;

  text-transform: uppercase;
  color: white;

  border: none;

  font-family: 'Roboto', sans-serif;
  font-optical-sizing: auto;
  font-weight: 400;
  font-style: normal;
  font-variation-settings: 'wdth' 100;
}
</style>
