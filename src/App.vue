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
  <router-view/>

  <!-- Hero footer: will stick at the bottom -->
  <div class="hero-foot">
      <div class="follow">
        <a href="#">LAST UPDATE 10.08.18</a>
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

.hero-foot{
  display: flex;
  font-size: 1.2rem;
  justify-content: space-between;
  padding: 0 1rem;
  text-transform: lowercase;
  opacity: 0.5;
}
.hero-body{
  a{
    background-image:
      linear-gradient(
        to bottom, #00D1B2 0%,
        #00D1B2 100%
    );
    background-position: 0 100%;
    background-repeat: repeat-x;
    background-size: 2px 2px;
    text-decoration: none;
    transition: all ease .2s;
    padding: 0px 2px;
    &:hover{
      // font-weight: bold;
      background-size: 4px 50px;
    }
  }
}
// #02B0AB
</style>
