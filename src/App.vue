<template>
  <div id="app">
    <HeaderComp :headerInfo="headerInfo"/>
    <MainComp :mainInfo="mainInfo"/>
    <FooterComp/>
  </div>
</template>

<script>
import HeaderComp from './components/HeaderComp.vue';
import MainComp from './components/MainComp.vue';
import FooterComp from './components/FooterComp.vue';

export default {
  name: 'App',
  components: {
    HeaderComp,
    MainComp,
    FooterComp
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
      },
      mainInfo: {
        coolData: [
          {
            data: "1.926",
            description: "finished sessions"
          },
          {
            data: "100%",
            description: "satisfaction rate"
          },
          {
            data: "3092+",
            description: "enrolled learners"
          },
          {
            data: "200",
            description: "online instructors"
          }
        ],
        videoInfo: {
          img: "home-movation-video-poster-670x450.jpg",
          description: "Every morning you have two choices: continue to sleep with your dreams, or wake up and chase them.",
          personName: "Kaixa Stark",
          personRole: "wingman",
          href: "#"
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
