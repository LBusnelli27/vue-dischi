<template>
  <div>
    <div class="card my-album-card" style="width: 18rem;">
      <img src="https://metalitalia.com/wp-content/uploads/2018/11/Queen-Queen-II-1974.png" class="card-img-top" alt="">
      <div class="card-body">
        <h2>Titolo</h2>
        <h5>Artista</h5>
        <p>1993</p>
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
      .then(response => (this.albumList = response.response))
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

  .my-album-card {
    background-color: $lightBlueGray;
    padding: 1rem;
    border-radius: .5rem;
    .card-body {
      text-align: center;
      h2 {
        color: white;
        margin-bottom: 2rem;
      }
      h5, p {
        color: $lightGray;
      }
    }
  }
</style>