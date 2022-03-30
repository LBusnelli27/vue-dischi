<template>
  <div>
    <div class="row">
      <div v-for="(element, index) in albumList" :key="index" class="card my-album-card">
        <img :src="element.poster" class="card-img-top" alt="">
        <div class="card-body">
          <h3>Titolo</h3>
          <h5>Artista</h5>
          <p>1993</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
import axios from 'axios';

export default {
  name: 'AlbumCard',

  data : function() {
    return{
      albumList : []
    }
  },
  mounted () {
    axios
      .get('https://flynn.boolean.careers/exercises/api/array/music')
      .then(response => (this.albumList = response.data.response));
  },
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

  .my-album-card {
    background-color: $lightBlueGray;
    padding: 1rem;
    margin: 1rem;
    border-radius: .5rem;
    width: calc((100% / 5) - 2rem);
    img {
      height: 50%;
    }
    .card-body {
      text-align: center;
      h3 {
        color: white;
        margin-bottom: 2rem;
      }
      h5, p {
        color: $lightGray;
      }
    }
  }
</style>