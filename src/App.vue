<!-- src/App.vue -->
<template>
  <div id="app">
    <MainNavbar />
    <router-view />
  </div>
</template>

<script>
import MainNavbar from './components/MainNavbar.vue';

export default {
  name: 'App',
  components: {
    MainNavbar,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  background-color: #000;
  background-image: url("@/assets/bg-img.jpeg");
  background-position: center;
  background-size: cover;
  height: 100vh;
  width: 100%;
}
</style>
