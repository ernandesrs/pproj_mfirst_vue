<template>
  <MainHeader />
  <MainMain />
  <MainFooter />
</template>

<script>

import MainHeader from './components/MainHeader.vue';
import MainMain from './components/MainMain.vue';
import MainFooter from './components/MainFooter.vue';

export default {
  name: 'App',
  components: {
    MainHeader,
    MainMain,
    MainFooter
  }
}

</script>

<style>
* {
  box-sizing: border-box;
}

body {
  background-color: #efefef;
  padding: 0;
  margin: 0;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
