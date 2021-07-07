<template>
  <div id="app">
    <div id="nav">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
    <router-view />
  </div>
</template>

<script>
import storage from './storage/index'
export default {
  data() {
    return {
      
    }
  },
  mounted() {
    storage.setItem({"user":{"a":1},"add":{"city":"suzhou","info":{"name":"q","num":{"n":3}}}})
    //storage.setItem('xxx','ccc','city')
    //storage.clear('a', 'user')
    console.log(storage.getItem('num','info'))
  },
}
</script>

<style lang="scss">
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}

#nav {
  padding: 30px;

  a {
    font-weight: bold;
    color: #2c3e50;

    &.router-link-exact-active {
      color: #42b983;
    }
  }
}
</style>
