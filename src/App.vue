<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
  <SideMenu />
  <MainPage />
  <RightSide />
</template>

<script>
import SideMenu from './components/SideMenu.vue'
import MainPage from './components/MainPage.vue'
import RightSide from './components/RightSide.vue'

export default {
  name: 'App',
  components: {
    SideMenu,
    MainPage,
    RightSide
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
