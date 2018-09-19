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
          <li><a href="#">home</a></li>
          <li><a href="#">about</a></li>
          <li><a href="#">contact</a></li>
        </ul>
      </nav>
      <p>last updated 9.16.18</p>
    </div>
    <div class="content">
      <!-- <h1>CONTENT</h1> -->
      <div class="about-me-home">
        <div class="about-me-title">
          <h2>|| About me ||</h2>
        </div>
        <div class="about-me-copy">
          <p>Hi, I'm Rudy Quevedo, a front end guy from Los Angeles, CA.
            I'm currently the Tech Lead for <a href="http://hi5.agency" target="_blank">&nbsp;hi5.agency </a>.
          </p>
          <p>
            For the last 12 years I've been in love with everything dev, always having something new to learn has fueled my passion for tech.
            I've had the luck of working in many different environments, building great web experiences to support a marketing campaigns, to educational software, to online product showcases.
          </p>
            <!-- Recently I've been really excited about building serveless projects, and fortunately have had the oppoturnity to launch
            the last two projects with <span class="vue">Vue.js</span>, <span class="aws">AWS API Gateway</span>, <span class="aws">AWS DynamoDB</span>, and <span class="aws">AWS Lambda</span>
          </p> -->

        </div>
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
@import url('https://fonts.googleapis.com/css?family=Oswald:400,700');
body{
  margin: 0px;
  font-family: 'Oswald', sans-serif;
}
#app {
  // font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  height: 100vh;
  overflow-x: hidden;
  overflow-y: auto;
  perspective: 1px;
  background: #fdffff;
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
  // background: #0B1013;
  font-family: "Helvetica Neue", Helvetica, Arial, sans-serif;

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
        font-size: 0.3em;
        font-weight: 400;
        display: inline;
        padding: 0px 0px 5px;
        border-bottom: 1px solid #fff;
        margin-left: 5px;
        a{
          color: #fff;
          text-decoration: none;
          text-transform: uppercase;
          padding-bottom: 2px;
          border-bottom:1px solid #fff;
        }
        &:hover{
          background:#fff;
          color: #000;
          transition: all ease 0.25s;
          border-bottom: 1px solid #000;
          a{
            color:#000;
            border-bottom:1px solid #000;
          }
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
    font-family: 'Oswald', sans-serif;
    width: 41%;
    text-align: right;
    margin-bottom: 5px;
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
  // background-image: url('./assets/rudy-hero.jpg');
  // background-image: url('./assets/dark.jpg');
  background-size: contain;
  background-repeat: no-repeat;
  background-color: #0B1013;
  // background-position: left top;
    background-position-x: right;
    background-position-y: bottom;
  @media screen and (min-width: $break-large){
    background-position-x: left;
    background-position-y: 120px;
    // background-size:auto;
  }
  // opacity: 0.4;
}
.content{
  height: 70vh;
  background-color: #FDFFFF;
  padding: 20px 10px;
  text-align: left;
  display: flex;
  justify-content: space-around;
  align-content: center;
  @media screen and (min-width: $break-large){
    height: 75vh;
  }
  .about-me-home{
    display: flex;
    flex-direction: row;
    flex-wrap: nowrap;
    flex:0 1 auto;
    align-content: stretch;
    align-items: flex-start;
    // padding: 1.5em;
    font-size: 1.2rem;
    line-height: 1.5em;
    a{
      background:#03B0AB;
      color: #fff;
      text-decoration: none;

    }
    @media screen and (min-width: $break-large){
      font-size: 2em;
    }
    .about-me-title{
      order: 0;
      flex: 0 1 auto;
      align-self: baseline;
      // height: 100%;
      writing-mode: tb-rl;
      text-align: left;
      margin-top: 1em;
      text-transform: uppercase;
      color: #fff;
      background: #0B1013;
      padding: 2em 0;
      h2{
        margin:0px 5px 0px 0px;
        line-height: 0.9em;
        letter-spacing: -1px;
        text-align: justify;
      }

    }
    .about-me-copy{
      order: 0;
      flex: 3 1 auto;
      align-self: auto;
      padding: 0px 20px;

    }
  }
  // margin-top: 20vh;
  .vue{

    text-decoration: underline dotted #42b883;
  }
  .aws{
    text-decoration: underline dotted #FF9900;
  }
}
// .hero{
//   display: flex;
//   height: 100%;
//   max-height: 250px;
//   flex-direction: row;
// }
</style>
