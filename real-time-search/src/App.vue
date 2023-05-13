<template>
  <div id="app">
    <img src="./assets/logo.png">
    <h1>Realtime Search Filter</h1>
    <h3>Made using Vue v2</h3>
    <h4>By <a href="https://www.linkedin.com/in/kaleb-iskandar-094423171/">Kalep</a></h4>
    <SearchFilter/>
  </div>
</template>

<script>
import SearchFilter from './components/SearchFilter'

export default {
  name: 'App',
  components: {
    SearchFilter
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
a {
  color: #42b983;
}
</style>
