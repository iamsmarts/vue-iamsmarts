<template>
  <div id="app">
    <!-- <Hero/>
    <router-view/> -->

    <div class="hero parallax">
      <!-- <h1>
          <span>front end dev</span><br>
          Rudy Quevedo
      </h1> -->
      <h1>
          <span>some not tot</span><br>
          some quezals
      </h1>
      <nav>
        <ul>
          <li>link 1</li>
          <li>link 2</li>
          <li>link 3</li>
        </ul>
      </nav>
      <p>last updated 9.16.18</p>
    </div>
    <div class="content">
      <!-- <h1>CONTENT</h1> -->
      <div class="about-me-home-copy">
      <p>Hi, I'm Rudy Quevedo, a front end developer from Los Angeles, CA.
        I'm currently the Tech Lead for <a href="http://hi5.agency" target="_blank"></a> hi5.agency
      </p>
      </div>
    </div>
  </div>
</template>

<script>
// import Hero from '@/components/Hero.vue'
export default {
  components: {
    // Hero,
  }
}
</script>


<style lang="scss">
$break-large: 1025px;
body{
  margin: 0px;
}
// nav{
//   height: 30px;
//   background-color:rgba(0 ,0, 0, 0.7);
//   position: fixed;
//   top: 0px;
//   left: 0px;
//   width: 100%;
// }
#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
  perspective: 1px;
  background: #000;
}
.hero {
  height: 80vh;
  display: flex;
  flex-direction: column;
  align-items: flex-end;
  justify-content: flex-end;
  font-size: 48px;
  color: white;
  padding-right: 10px;
  @media screen and (min-width: $break-large){
    align-items: flex-end;
  }
  h1{
    // background-color:pink;
    margin: 0px;
    font-size: 0.5em;
    line-height: 20px;
    letter-spacing: -2px;
    text-transform: uppercase;
    text-align: justify;
    @media screen and (min-width: $break-large){
      writing-mode: horizontal-tb;
      transform: none;
    }
  }
  nav{
      display:flex;
      justify-content:center;
      ul{
      list-style: none;
      display: flex;
      // flex-direction: row;
      // background:#2c3e50;
      justify-content: space-around;
      margin: 5px 0px;
      padding: 0px;
      li{
        font-size: 0.4em;
        // border-right: 1px solid #fff;
        display: inline;
        padding: 5px;
        &:hover{
          background:#fff;
          color: #000;
          transition: all ease 0.25s;
        }
        // display: inline-block;
      }
    }
  }
  p{
    font-size: 0.3em;
    margin: 0px;
    padding: 4px;
    background:#fff;
    color: #000;
    text-transform: uppercase;
  }

}
.parallax::after {
  content: " ";
  position: absolute;
  top: 0;
  right: 0;
  bottom: 0;
  left: 0;
  transform: translateZ(-1px) scale(2);
  z-index: -1;
  background-image: url('./assets/dark.jpg');
  background-size: contain;
  background-repeat: no-repeat;
  background-color: #000;
  @media screen and (min-width: $break-large){
    background-size:auto;
  }
  opacity: 0.4;
}
.content{
  height: 70vh;
  background-color: #000;
  padding: 20px 10px;
  text-align: justify;
  display: flex;
  justify-content: space-around;
  align-content: center;
  @media screen and (min-width: $break-large){
    height: 75vh;
  }
  .about-me-home-copy{
    padding: 1.5em;
    font-size: 1.6em;
    @media screen and (min-width: $break-large){
      font-size: 2em;
    }
  }
  // margin-top: 20vh;

}
// .hero{
//   display: flex;
//   height: 100%;
//   max-height: 250px;
//   flex-direction: row;
// }
</style>
