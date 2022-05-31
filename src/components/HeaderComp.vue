<template>
  <header>
    <div class="container">
      <div class="top-header">
        <div class="logo">
          <img src="../assets/img/dark-logo.png" alt="Logo">
        </div>
        <ul class="top-menu">
          <li
            v-for="(menuOption, index) in headerInfo.menuOptions"
            :key="`topMenu-${index}`">
            <a :href="menuOption.href">{{menuOption.name}}<i class="fa-solid fa-chevron-down"></i></a>
          </li>
        </ul>
        <ul class="socials">
          <li
            v-for="(socialClass, index) in headerInfo.socialClasses"
            :key="`socials-${index}`">
            <a :href="socialClass.href"><i :class="socialClass.name"></i></a>
          </li>
        </ul>
      </div>
      
      <div class="jumbotron">
        <div class="left-jumbo">
          <h6>I'M WINGMAN</h6>
          <h1 class="title">Peace On Earth A Wonderful Wish But No Way</h1>
          <p>Success isn't overnight. It's when everyday you get a little better than the day before. It all adds up.</p>
          <ButtonComp :buttonInfo="headerInfo.buttonInfo"/>
        </div>
        <div class="right-jumbo">
          <img class="background" src="../assets/img/home-movation-shape-face.png" alt="">
          <img class="person" src="../assets/img/home-movation-hero-image.png" alt="">
        </div>
      </div>
    </div>
    <ul class="side-tools">
      <li
        v-for="(sideTool, index) in headerInfo.sideTools"
        :key="`sideTools-${index}`">
        <a :href="sideTool.href"><i :class="sideTool.name"></i></a>
      </li>
    </ul>
  </header>
</template>

<script>
import ButtonComp from './ButtonComp.vue';
export default {
  name: "HeaderComp",
  props: {
    headerInfo: Object,
  },
  components: { 
    ButtonComp
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

header{
  position: relative;
  background-image: $background-pattern-wavify;
  background-color: #f7f7fd; 
  font-size: 15px;
  margin-bottom: 123px;
  overflow: hidden;
  .top-header{
    display: flex;
    justify-content: space-between;
    align-items: center;
    min-height: 80px;
    width: 100%;
    margin-bottom: 57px;
    .logo{
      max-width: 157px;
    }
    ul{
      li a{
        display: inline-flex;
        align-items: center;
        color: #3b3661;
      }
    }
    .top-menu{
      li{
        margin: 0 12px 0 27px;
      }
      i{
        font-size: 7px;
        margin-left: 6px;
      }
    }
    .socials{
      a{
        font-size: 17px;
        margin: 0 12px;
      }
    }
  }
  .side-tools{
    position: absolute;
    top: 200px;
    right: 0;
    width: 40px;
    background-color: white;
    box-shadow: 0px 0px 10px 2px lightgray;
    border-radius: 5px 0 0 5px;
    overflow: hidden;
    li{
      display: block;
      width: 100%;
      height: 40px;
    }
    a{
      display: inline-flex;
      justify-content: center;
      align-items: center;
      width: 100%;
      height: 100%;
      font-size: 16px;
      color: black;
      transition: all .15s linear;
      &:hover{
        background-color: lightgray;
      }
    }
  }
  .jumbotron{
    position: relative;
    display: flex;
    width: 100%;
    .left-jumbo,
    .right-jumbo{
      width: 50%;
      // height: fit-content;
    }
    .left-jumbo{
      padding: 75px 120px 149px 0;
      h6{
        font-size: 15px;
        margin-bottom: 17px;
      }
      h1{
        font-size: 56px;
        line-height: 75px;
        margin-bottom: 23px;
      }
      p{
        line-height: 30px;
        margin-bottom: 34px;
      }
    }
    .right-jumbo{
      position: absolute;
      bottom: 0;
      left: 50%;
      .person{
        position: absolute;
        bottom: 0;
        left: 0;
        z-index: 3;
      }
      .background{
        position: absolute;
        bottom: -50px;
        left: 60px;
        width: 95%;
      }
    }
  }
}
</style>