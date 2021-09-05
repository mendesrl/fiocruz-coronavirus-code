<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png"> -->
    <!-- <HelloWorld msg="Welcome to Your Vue.js App"/> -->
    <Header />
    <Body />
  </div>
</template>

<script>
// import HelloWorld from './components/HelloWorld.vue';
import Header from './components/Header.vue';
import Body from './components/Body.vue';


export default {
  name: 'App',
  components: {
    Header,
    Body
  }
}
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin: auto;
  max-width: 10000px;
  display: grid;
  grid-template-columns: 1fr;
  justify-content: center;
}
</style>
