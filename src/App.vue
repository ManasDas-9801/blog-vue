<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
  
    <Class />
  </div>
  
</template>

<script>
 import Class from './components/Style.vue';
export default {
  name: 'App',
  components: {
    Class
     
      
  }
};
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
