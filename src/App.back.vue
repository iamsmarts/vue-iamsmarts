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
          <h2>|| About me</h2>
        </div>
        <div class="about-me-copy">
          <p>Hi I'm Rudy - Currently Tech Lead at <a href="http://hi5.agency" class="hi5">hi5.agency</a>, previously I was the Senior Front End Developer at <a href="http://ignitioncreative.com/" class="ignition">ignition creative</a>. When my nose isn't buried in code, I'm heavy into gaming whether its on one of the new gen consoles, pc, or even some board games.</p>

          <p><strong>What I'm into right now:</strong> Recently I have been spending sometime with <a href="https://vuejs.org/" class="vue">Vue.js</a>, and used vue on our last two launched projects.</p>

          <p><strong>Current Favorite Resource:</strong>On my drive in to work and at the gym Wes Bos and Scott Tolinski's <a href="https://syntax.fm/" class="syntax">syntax.fm</a> Podcast is my go to. I also find a ton of gems in <a href="https://frontendfoc.us/" class="fefocus">Frontend Focus</a> newsletter. </p>


          <!-- <p>Hi, I'm Rudy Quevedo, a front end guy from Los Angeles, CA.
            I'm currently the Tech Lead for <a href="http://hi5.agency" target="_blank">&nbsp;hi5.agency </a>.
          </p>
          <p>
            For the last 12 years I've been in love with everything dev, always having something new to learn has fueled my passion for tech.
            I've had the luck of working in many different environments, building great web experiences to support a marketing campaigns, to educational software, to online product showcases.
          </p> -->
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
:root {
  --mainColor: #ff9800;
}
@import url('https://fonts.googleapis.com/css?family=Oswald:400,700');
body{
  margin: 0px;
  font-family: 'Oswald', sans-serif;
}
#app {
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
    font-size: 1.2rem;
    line-height: 1.4em;
    a{
      background-position: 0 100%;
      background-repeat: repeat-x;
      background-size: 4px 4px;
      text-decoration: none;
      transition: all ease .2s;
      padding: 0px 2px;
      &:hover{
        background-size: 4px 50px;
      }
    }

    .hi5{
      background-image:
        linear-gradient(
          to bottom, #07b0ab 0%,
          #07b0ab 100%
      );
      color: #07b0ab;

      &:hover{
        color:#fff;
      }
    }
    .vue{
      background-image:
        linear-gradient(
          to bottom, rgba(107, 185, 134, 1) 0%,
          rgba(107, 185, 134, 1) 100%
      );
      color: rgba(107, 185, 134, 1);
      &:hover{
        color:  #fff;
      }
    }
    .syntax{
      background-image:
        linear-gradient(
          to bottom, rgba(226, 188, 106, 1) 0%,
          rgba(226, 188, 106, 1) 100%
      );
      color: #000;
    }
    .fefocus{
      background-image:
        linear-gradient(
          to bottom, rgba(225, 109, 60, 1) 0%,
          rgba(225, 109, 60, 1) 100%
      );
      color: rgba(225, 109, 60, 1);
      &:hover{
        color:#fff;
      }
    }
    .ignition{
      // background: rgba(179, 37, 53, 0.6);
      background-image:
        linear-gradient(
          to bottom, rgba(179, 37, 53, 1) 0%,
          rgba(179, 37, 53, 1) 100%
      );
      color: rgba(179, 37, 53, 1);
      &:hover{
        color:  #fff;
      }
    }

    @media screen and (min-width: $break-large){
      font-size: 2em;
    }
    .about-me-title{
      order: 0;
      flex: 0 1 auto;
      align-self: normal;
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
  .vue{
    text-decoration: underline dotted #42b883;
  }
  .aws{
    text-decoration: underline dotted #FF9900;
  }
}
</style>
