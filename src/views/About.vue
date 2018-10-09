<template>
  <div class="hero-body about-body ">
    <div class="container columns is-mobile is-centered">
      <div class="column is-full-mobile is-three-quarters-tablet about-copy ">
        <h1>Hi I'm Rudy,</h1>
        <p class="bio">For the past 14 years I have been sharpening my skills in Javascript, HTML, and CSS, keeping that day one curiosity to learn. Along my journey I have had the pleasure of working in a variety of different teams, rolling my sleeves up in startups, learning the product, to keeping pace in the fast moving world of creative agencies. These experiences have exposed me to many challenges, which have gave me a keen sense of problem solving and humble approach to working within any size team.</p>
        <p><strong>What I'm into right now:</strong> Recently I have been spending sometime with <a href="https://vuejs.org/" class="vue">Vue.js</a>, and used vue on our last two launched projects.</p>
        <p><strong>Current Favorite Resource:</strong> On my drive in to work and at the gym Wes Bos and Scott Tolinski's <a href="https://syntax.fm/" class="syntax">syntax.fm</a> Podcast is my go to. I also find a ton of gems in <a href="https://frontendfoc.us/" class="fefocus">Frontend Focus</a> newsletter. </p>
      </div>
    </div>
  </div>
</template>


<script>
export default {
  name: 'About'
}
</script>

<style lang="scss" scoped>
.about-copy{
  // background: salmon;
  .bio {
      margin: 0 0 1.5rem 0;
  }
  p{
    font-size:1.6rem;
    margin: 1.5rem 0rem;
    line-height: 2.2rem;
  }
}
</style>

