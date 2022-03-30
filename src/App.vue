<template>
  <div id="app">
    <Header />
    <Main />
    <AlbumCard />
  </div>
</template>

<script>
import 'bootstrap/dist/css/bootstrap.css';

import Header from './components/Header.vue';
import Main from './components/Main.vue';
import AlbumCard from './components/AlbumCard.vue';

export default {
  name: 'App',
  components: {
    Header,
    Main,
    AlbumCard
  }
}
</script>

<style lang="scss" scoped>
  @import "./assets/scss/style.scss";
</style>
