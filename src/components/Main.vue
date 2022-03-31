<template>
  <div class="my-bg-main">
    <div class="row">
      <div class="col-12">
        <select v-model="inputGenre" class="form-select mb-5 me-3 d-inline my-select-type" aria-label="Default select example">
          <option value="default" selected>Select a genre</option>
          <option value="rock">Rock</option>
          <option value="metal">Metal</option>
          <option value="pop">Pop</option>
          <option value="jazz">Jazz</option>
        </select>
      </div>
    </div>
    <AlbumCard :input-select="inputGenre"/>
  </div>
</template>

<script>
import AlbumCard from './AlbumCard.vue';

export default {
  name: 'MainSection',

  data: function() {
    return {
      inputGenre : ''
    }
  },

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
    .my-select-type {
      width: 20%;
    }
  }
</style>