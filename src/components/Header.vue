<template>
  <div>
    <nav class="navbar navbar-light">
      <div class="container-fluid">
        <img src="https://cdn-icons-png.flaticon.com/512/174/174872.png" alt="Spotify Logo">
      </div>
    </nav>
  </div>
</template>

<script>
export default {
  name: 'HeaderSection',
}
</script>

<style lang="scss" scoped>
@import "../assets/scss/style.scss";

  div {
    nav{
      background-color: $lightBlueGray;
      img {
        height: 60px;
      }
    }
  }
</style>