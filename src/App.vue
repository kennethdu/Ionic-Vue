<template>
  <div id="app">
        <img alt="r/pics logo" src="https://styles.redditmedia.com/t5_2qh0u/styles/bannerPositionedImage_ssrvude96kzz.png">

    <div id="nav">
    </div>
    <router-view/>
  </div>
</template>

<style>

#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
#nav {
  padding: 30px;
}
#nav a {
  font-weight: bold;
  color: #2c3e50;
}
#nav a.router-link-exact-active {
  color: #42b983;
}

</style>
