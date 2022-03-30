<template>
  <div>
    <div class="row">
      <div v-for="(element, index) in albumList" :key="index" class="card my-album-card">
        <img :src="element.poster" class="card-img-top" alt="">
        <div class="card-body">
          <h3 class="fw-bold text-uppercase">{{ element.title }}</h3>
          <h5>{{ element.author }}</h5>
          <p>{{ element.year }}</p>
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
      height: 60%;
    }
    .card-body {
      text-align: center;
      h3 {
        color: white;
        margin-bottom: 2rem;
        font-size: 1.2rem;
      }
      h5, p {
        color: $lightGray;
        font-size: 1rem;
      }
    }
  }
</style>