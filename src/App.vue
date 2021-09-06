<template>
  <div id="app">
    <Header />
    <Body />
  </div>
</template>

<script>
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
  font-family: Roboto,Avenir, Helvetica, Arial, sans-serif;
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
