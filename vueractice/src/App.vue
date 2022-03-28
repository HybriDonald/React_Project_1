<template>
  <div class="menu">
    <h1 class="title">게시판 샘플</h1>
      <a v-for="category in categories" v-bind:key="category">{{ category }}</a>
  </div>
  <img alt="Vue logo" src="./assets/logo.png">

  <div>
    <router-view>
    </router-view>
  </div>
</template>

<script>

export default {
  name: 'App',
  data() {
    return {
      link : {
        categories : ['자유게시판', '개드립', '익명게시판'],
        link : ['']
      },
      
    }
  },
  component : {
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}

.menu {
  background-color: #2c3e50;
  border-radius: 10px;
  font-family: 'NanumGothic';
}

.title {
  color: white;
}

a {
  color: white;
  padding: 10px;
}

@font-face {
  font-family: 'NanumGothic';
  src: url('assets/fonts/NanumGothic.ttf') format('truetype');
  font-weight: 300;
}

</style>
