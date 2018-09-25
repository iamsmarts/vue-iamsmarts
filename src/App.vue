<template>
  <div id="app">
    <!-- <Hero/>
    <router-view/> -->
    <!-- nav -->
    <!-- <Navi/> -->
<section class="hero is-dark is-fullheight">
  <!-- Hero head: will stick at the top -->
  <div class="hero-head">
    <Navi/>
  </div>

  <!-- Hero content: will be in the middle -->
  <div class="hero-body home-body">
    <div class="container columns is-gapless">
      <div class="copy column is-three-quarters-mobile">
        <h1>Hi I'm Rudy Quevedo</h1>
        <p>Passionate about Front End Development</p>
      </div>
      <div class="home-button-wrap">
        <a href="#"  class="button is-outlined">More About Me</a>
        <a href="#"  class="button is-outlined">My Experience</a>
      </div>
    </div>
  </div>

  <!-- Hero footer: will stick at the bottom -->
  <div class="hero-foot">
    <div class="follow">
      <a href="#">@iamsmarts</a>
    </div>
    <div class="built">
      <p>powered by <a href="#">vue</a> using <a href="#">Bulma</a></p>
    </div>
  </div>
</section>
  </div>
</template>

<script>
// import Hero from '@/components/Hero.vue'
import Navi from '@/components/Nav';
export default {
  components: {
    Navi,
  },
}
</script>


<style lang="scss">

@import url('https://fonts.googleapis.com/css?family=Oswald:400,700');
.home-body::after{
  content: "";
  background-image: url('./assets/rudy-hero2.png');
  background-size: contain;
  background-repeat: no-repeat;
  background-position-x: calc(100% + 80px);
  opacity: 0.05;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
  position: absolute;
  z-index: -1;
}
.home-button-wrap{
  display: flex;
  justify-content: space-between;
  padding: 0.75em;
  .button{
    background:transparent;
    color: #fff;
  }
}
</style>
