<template>
  <div id="app">
    <Header />
    <Main />
    <AlbumCard />
  </div>
</template>

<script>
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

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
