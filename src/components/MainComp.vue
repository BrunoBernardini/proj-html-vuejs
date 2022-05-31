<template>
  <main>
    <div class="container">
      <ul class="cool-data">
        <li
          v-for="(singleCoolData, index) in mainInfo.coolData"
          :key="`coolData-${index}`">
          <img src="../assets/img/background-pattern-grid-line-06.png" alt="Grid-line">
          <div class="text-cell">
            <h2 class="highlight">{{singleCoolData.data}}</h2>
            <span>{{singleCoolData.description.toUpperCase()}}</span>
          </div>
          <img class="last-line" src="../assets/img/background-pattern-grid-line-06.png" alt="Grid-line">
        </li>
      </ul>

      <section class="about">
        <div class="left-half">
          <span class="highlight">ABOUT ME</span>
          <h1 class="title">How to Be an Alpha Male: The 15 Habits of True Alphas</h1>
        </div>
        <div class="right-half">
          <h6>Want to learn ho to be <span class="highlight">an alpha male</span>? How to be more masculine? How to be the man you've always wanted to be?</h6>
          <p>Your goal is to show the consistency of business, core values, and customer care. Punctuality, responsibility, individuality, accuracy, enthusiasm - you have to clearly explain how these qualities are applicable to your work. And the important thing is you do love what you do.</p>
        </div>
      </section>

      <YoutubeVideoSection :videoInfo="mainInfo.videoInfo"/>

      <section class="courses">
        <p>begin your journey at maxcoach</p>
        <h1 class="title">Latest <span class="highlight">Online Courses</span></h1>
      </section>
    </div>
  </main>
</template>

<script>
import YoutubeVideoSection from './YoutubeVideoSection.vue';
export default {
  name: "MainComp",
  props: {
    mainInfo: Object,
  },
  components: {
    YoutubeVideoSection
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

main{
  .cool-data{
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    margin-bottom: 133px;
    li{
      position: relative;
      .text-cell{
        position: absolute;
        top: 50%;
        left: 50%;
        transform: translate(-50%, -50%);
        text-align: center;
        h2{
          font-size: 36px;
          font-weight: bolder;
          margin-bottom: 14px;
        }
        span{
          font-size: 15px;
        }
      }
      .last-line{
        position: absolute;
        top: 0;
        right: -1px;
        -webkit-transform: scaleX(-1);
        transform: scaleX(-1);
      }
    }
  }
  .about{
    display: flex;
    align-items: flex-end;
    margin-bottom: 92px;
    .left-half,
    .right-half{
      width: 50%;
    }
    .left-half{
      padding-right: 140px;
      span{
        display: inline-block;
        font-size: 14px;
        margin-bottom: 23px;
      }
      h1{
        line-height: 60px;
      }
    }
    .right-half{
      h6{
        font-size: 17px;
        line-height: 32px;
        margin-bottom: 15px;
      }
      p{
        font-size: 14px;
        line-height: 24px;
      }
    }
  }
  .courses{
    text-align: center;
    p{
      text-transform: uppercase;
      font-size: 14px;
      margin-bottom: 21px;
    }
    h1{
      font-size: 49px;
      color: $secondary-color;
      margin-bottom: 68px;
    }
  }
}
</style>