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
            <a class="navbar-item is-active">
              Home
            </a>
            <a class="navbar-item">
              Examples
            </a>
            <a class="navbar-item">
              Documentation
            </a>
            <span class="navbar-item">
              <a class="button is-primary is-inverted">
                <span class="icon">
                  <i class="fab fa-github"></i>
                </span>
                <span>Download</span>
              </a>
            </span>
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
