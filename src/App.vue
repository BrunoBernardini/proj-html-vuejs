<template>
  <div id="app">
    <HeaderComp
      :headerInfo="headerInfo"/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';

export default {
  name: 'App',
  components: {
    HeaderComp
  },
  data(){
    return{
      headerInfo: {
        menuOptions: [
          {
            name: "Home",
            href: "#"
          },
          {
            name: "Pages",
            href: "#"
          },
          {
            name: "Courses",
            href: "#"
          },
          {
            name: "Features",
            href: "#"
          },
          {
            name: "Blog",
            href: "#"
          },
          {
            name: "Shop",
            href: "#"
          }
        ],
        socialClasses: [
          {
            name: "fa-brands fa-twitter",
            href: "#"
          },
          {
            name: "fa-brands fa-facebook-f",
            href: "#"
          },
          {
            name: "fa-brands fa-instagram",
            href: "#"
          },
          {
            name: "fa-brands fa-linkedin",
            href: "#"
          }
        ],
        sideTools: [
          {
            name: "fa-solid fa-ruler",
            href: "#"
          },
          {
            name: "fa-solid fa-life-ring",
            href: "#"
          },
          {
            name: "fa-solid fa-book",
            href: "#"
          },
          {
            name: "fa-solid fa-cart-shopping",
            href: "#"
          }
        ],
        buttonInfo: {
          name: "Get Started for free",
          href: "#",
          arrow: true
        }
      }
    }
  }
}
</script>

<style lang="scss">
@import "./assets/style/vars";
@import "./assets/style/general";

#app {
  
}
</style>
