<template>
  <div id="app">
    <Hero/>
    <router-view/>
  </div>
</template>

<script>
import Hero from '@/components/Hero.vue'
export default {
  components: {
    Hero,
  }
}
</script>


<style lang="scss">
body{
  margin: 0px;
}
#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
}
.hero{
  display: flex;
  height: 100%;
  max-height: 250px;
  flex-direction: row;
}
</style>
