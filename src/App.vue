<template>
  <div id="app">
    <Header />
    <Main />
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';

import Header from './components/Header.vue';
import Main from './components/Main.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main
  }
}
</script>

<style lang="scss" scoped>
  
</style>
