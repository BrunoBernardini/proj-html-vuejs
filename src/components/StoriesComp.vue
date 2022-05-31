<template>
  <section class="stories-component">
    <div class="text-box">
      <div
        v-for="(storyInfo, index) in storiesInfo"
        :key="`storyInfo-${index}`"
        class="content"
        :class="{'active': index==activeIndex}">
        <span class="highlight upper-text">REAL STORIES</span>
        <h2>{{storyInfo.story}}</h2>
        <div class="avatar">
          <img :src="getImgUrl(storyInfo.avatar)" alt="Avatar">
        </div>
        <h3>{{storyInfo.name}}</h3>
        <p>{{storyInfo.job}}</p>
      </div>
    </div>
    <div class="img-box">
      <img src="../assets/img/home-movation-testimonial-image.jpg" alt="">
    </div>
    <div class="controller">
      <img
        @click="incrementIndex()"
        src="../assets/img/image.png"
        alt="Up">
      <h5>{{activeIndex+1}}/{{storiesInfo.length}}</h5>
      <img
        @click="decrementIndex()"
        src="../assets/img/image (1).png"
        alt="Down">
    </div>
  </section>
</template>

<script>
export default {
  name: "StoriesComp",
  props:{
    storiesInfo: Array
  },
  data(){
    return{
      activeIndex: 0
    }
  },
  methods:{
    getImgUrl(img){
      return require("../assets/img/"+img);
    },
    incrementIndex(){
      if(this.activeIndex+1 === this.storiesInfo.length) this.activeIndex = 0;
      else this.activeIndex++
    },
    decrementIndex(){
      if(this.activeIndex-1 < 0) this.activeIndex = this.storiesInfo.length-1;
      else this.activeIndex--
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

.stories-component{
  display: flex;
  position: relative;
  overflow: hidden;
  margin-bottom: 147px;
  .text-box,
  .img-box{
    width: 50%;
    height: 701px;
  }
  .text-box{
    position: relative;
    background-image: $background-pattern-wavify;
    background-color: #f7f7fd;
    .content{
      position: absolute;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      padding: 220px;
      text-align: center;
      opacity: 0;
      transition: all .15s;
      &.active{
        opacity: 1;
      }
      .upper-text{
        font-size: 14px;
        font-weight: bold;
        margin-bottom: 55px;
      }
      h2{
        font-size: 24px;
        line-height: 40px;
        margin-bottom: 55px;
      }
      .avatar{
        flex-shrink: 0;
        width: 85px;
        height: 85px;
        border-radius: 50%;
        overflow: hidden;
        margin-bottom: 27px;
      }
      h3{
        font-size: 20px;
        margin-bottom: 14.5px;
      }
      p{
        font-size: 14px;
      }
    }
  }
  .img-box{
    img{
      width: 100%;
    }
  }
  .controller{
    position: absolute;
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    top: 51%;
    left: 50%;
    transform: translate(-50%, -51%);
    width: 94px;
    height: 94px;
    border-radius: 50%;
    background-color: white;
    box-shadow: 0 0 10px lightgray;
    h5{
      font-size: 16px;
      margin: 11px 0 14px 0;
    }
    img:hover{
      cursor: pointer;
    }
  }
}
</style>