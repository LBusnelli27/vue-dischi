<template>
  <div class="my-bg-main">
    <AlbumCard />
  </div>
</template>

<script>
import AlbumCard from './AlbumCard.vue';

export default {
  name: 'MainSection',
  components : {
    AlbumCard
  },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

  .my-bg-main {
    background-color: $darkBlueGray;

    padding: 5rem 10%;
  }
</style>