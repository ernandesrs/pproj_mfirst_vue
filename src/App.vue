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
    MainFooter,
  },
}

</script>

<style>
* {
  box-sizing: border-box;
}

body {
  background-color: #e8e8e8;
  min-height: 100vh;
  padding: 0;
  margin: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;

  background-color: #f2f2f2;
  width: 100%;
  max-width: 475px;
  border: solid 1px #ccc;
  padding: 20px;
  border-radius: 3px;
  box-shadow: 0 0 18px 0 #2c3e502e;
}
</style>
