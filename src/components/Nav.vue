<template>
    <nav class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item">
            <img src="https://bulma.io/images/bulma-type-white.png" alt="Logo">
          </a>
          <span class="navbar-burger burger" data-target="navbarMenuHeroA" @click="toggleNav">
            <span></span>
            <span></span>
            <span></span>
          </span>
        </div>
        <div id="navbarMenuHeroA" :class="[{'is-active':mobileNav}, 'navbar-menu']">
          <div class="navbar-end">
            <router-link to="/home" class="navbar-item is-active">
              Home
            </router-link>
            <router-link to="/about" class="navbar-item">
            About
            </router-link>
            <router-link to="/resume" class="navbar-item">
              CV
            </router-link>
            <!-- <span class="navbar-item">
              <a class="button is-primary is-inverted">
                <span class="icon">
                  <i class="fab fa-github"></i>
                </span>
                <span>Download</span>
              </a>
            </span> -->
          </div>
        </div>
      </div>
    </nav>

</template>
<script>
export default {
  data(){
    return{
      mobileNav:false,
    }
  },
  methods:{
    toggleNav:function(){
        console.log('toggling')
      this.mobileNav = !this.mobileNav;
    }
  }
}
</script>
<style lang="scss">
.navbar{
    background-color: transparent;
    .navbar-brand{
        .navbar-item{
            &.brand{
                flex-direction: column;
                align-items: flex-start;
            }
        }
    }

}
</style>
