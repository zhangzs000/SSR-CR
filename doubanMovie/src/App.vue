<template>
  <div id="app"  exclude="moviesDetail">
    <Dheader></Dheader>
    <transition name="fade">
    <router-view/>
    </transition>
  </div>
</template>

<script>
export default {
  name: 'App',
  data(){
    return {
      msg: 'xxx'
    }
  },
  components: {
    'Dheader': (resolve) => {
      require(['./header'], resolve)
    }
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
