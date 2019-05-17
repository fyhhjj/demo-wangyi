<template>
  <div id="app">
    <div id="nav">
      <router-view></router-view>
    </div>
  </div>
</template>

<style lang="less">
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #666;
  padding: 10px;
}
#nav {
  a {
    font-weight: bold;
    color: #666;
    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
