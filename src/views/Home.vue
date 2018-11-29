<template>
  <div class="hero-body home-body">
    <div class="container columns">
      <div class="home-copy column is-6-desktop is-offset-3">
        <h1>Hi I'm Rudy Quevedo</h1>
        <p>Tech Lead at <a href="http://hi5.agency" target="_blank" class="hi5">hi5.agency</a></p>
        <p>Builder of things on the web</p>
        <p>Avid gamer and soccer afficionado</p>
        <router-link to="/about">More about me</router-link> || <router-link to="/resume">My resume</router-link>
        <p class="small"><em>work on going - last update 10/10/18</em></p>
      </div>
    </div>
  </div>
</template>

<script>
// @ is an alias to /src
// import HelloWorld from '@/components/HelloWorld.vue'

export default {
  name: 'Home',

}
</script>
<style lang="scss" scoped>

.home-body::after{
  content: "";
  background-image: url('../assets/rudy-hero2.png');
  background-size: cover;
  background-repeat: no-repeat;
  background-position-x: calc(100% + 80px);
  opacity: 0.1;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;
}
  @media (min-width: 960px){
    .home-body::after{
      background-size:contain;
    }
  }
.home-copy{
  font-size: 2rem;
}
.home-copy h1{
  font-size: 2.8rem;
}
.small{
  font-size: 1.2rem;
}
</style>
