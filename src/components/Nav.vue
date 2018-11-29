<template>
    <nav class="navbar">
      <div class="container">
        <div class="navbar-brand">
          <a class="navbar-item">
            <img src="@/assets/iamsmarts-type-white-alt.png" alt="Logo">
          </a>
          <span class="navbar-burger burger" data-target="navbarMenuHeroA" @click="toggleNav">
            <span></span>
            <span></span>
            <span></span>
          </span>
        </div>
        <div id="navbarMenuHeroA" :class="[{'is-active':mobileNav}, 'navbar-menu']">
          <div class="navbar-end">
            <router-link to="/" :class="[{'is-active':pageActive('Home')}, , 'navbar-item']" >
              Home
            </router-link>
            <router-link to="/about" :class="[{'is-active':pageActive('About')}, , 'navbar-item']" >
              About
            </router-link>
            <router-link to="/resume" :class="[{'is-active':pageActive('Resume')}, , 'navbar-item']" >
              Resume
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
  props:['mobileNavHandle'],
  data(){
    return{
      mobileNav:false,
      pageName: null,
    }
  },
  beforeMount(){
    this.pageName = this.$route.name;
  },
  mounted(){
    this.$router.afterEach(() => {
      this.mobileNav = false;
    })
  },
  methods:{
    toggleNav:function(){
      // console.log('toggling');
      this.mobileNav = !this.mobileNav;
    },
    pageActive: function(linkName){
      return this.$route.name === linkName;
    },
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
