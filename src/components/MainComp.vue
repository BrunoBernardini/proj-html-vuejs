<template>
  <main>
    <section class="container">
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
        <div class="course-cards-container">
          <CourseCard
            v-for="(courseInfo, index) in mainInfo.coursesInfo.coursesCards"
            :key="`courseInfo-${index}`"
            :courseInfo="courseInfo"/>
        </div>
        <ButtonComp :buttonInfo="mainInfo.coursesInfo.buttonInfo"/>
      </section>

      <section class="books">
        <div class="text-box">
          <span class="upper-text">book store online</span>
          <h1 class="title">Be Alpha With <span class="highlight">Wingman's Book</span></h1>
          <ul class="fa-ul">
            <li 
              v-for="(checkOption, index) in mainInfo.booksInfo.checkList"
              :key="`checkOption-${index}`">
              <span class="fa-li"><i class="fa-solid fa-check"></i></span>
              <span class="list-el">{{checkOption}}</span>
            </li>
          </ul>
          <ButtonComp :buttonInfo="mainInfo.booksInfo.buttonInfo"/>
        </div>

        <div class="books-box">
          <BookCard
            v-for="(bookCard, index) in mainInfo.booksInfo.booksCards"
            :key="`bookCard-${index}`"
            :bookInfo="bookCard"
            :bookMenuOptions="mainInfo.booksInfo.bookMenuOptions"/>
        </div>
      </section>

      <section class="partners">
        <a
          v-for="(partner, index) in mainInfo.partnersInfo"
          :key="`partner-${index}`"
          :href="partner.href">
          <img
            :src="getImgUrl(partner.img)"
            :alt="partner.img">
        </a>
      </section>
    </section>

    <StoriesComp :storiesInfo="mainInfo.storiesInfo"/>

    <section class="container">
      <section class="blog">
        <span class="upper-text">BLOG UPDATED</span>
        <h1 class="title">Interesting <span class="highlight">articles updated</span> daily</h1>
        <div class="articles-container">
          <ArticleCard
            v-for="(articleInfo, index) in mainInfo.articlesInfo.articleCards"
            :key="`articleInfo-${index}`"
            :articleInfo="articleInfo"/>
        </div>
        <a
          :href="mainInfo.articlesInfo.viewMoreHref"
          class="highlight">View all posts</a>
      </section>
    </section>
  </main>
</template>

<script>
import YoutubeVideoSection from './YoutubeVideoSection.vue';
import CourseCard from './CourseCard.vue';
import ButtonComp from './ButtonComp.vue';
import BookCard from './BookCard.vue';
import StoriesComp from './StoriesComp.vue';
import ArticleCard from './ArticleCard.vue';

export default {
  name: "MainComp",
  props: {
    mainInfo: Object,
  },
  components: {
    YoutubeVideoSection,
    CourseCard,
    ButtonComp,
    BookCard,
    StoriesComp,
    ArticleCard
},
  methods: {
    getImgUrl(img){
      return require("../assets/img/"+img);
    }
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
    margin-bottom: 108px;
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
    .course-cards-container{
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      margin-bottom: 36px;
    }
  }
  .books{
    display: flex;
    justify-content: space-between;
    margin-bottom: 153px;
    .text-box{
      width: 310px;
      .upper-text{
        display: block;
        text-transform: uppercase;
        font-size: 14px;
        margin-bottom: 13px;
      }
      h1{
        color: $secondary-color;
        line-height: 60px;
        margin-bottom: 29px;
      }
      .fa-ul {
        margin: 0 0 42px 30px;
        li{
          display: block;
          color: gray;
          margin-bottom: 11px;
        }
        i{
          color: $main-color;
        }
        .list-el{
          font-size: 14px;
        }
      }
    }
    .books-box{
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
    }
  }
  .partners{
    display: flex;
    justify-content: space-between;
    align-items: center;
    filter: brightness(0) saturate(100%) invert(100%) sepia(55%) saturate(295%) hue-rotate(140deg) brightness(93%) contrast(84%);
    margin-bottom: 150px;
  }
  .blog{
    .upper-text{
      display: block;
      font-size: 14px;
      margin-bottom: 19px;
    }
    h1{
      margin-bottom: 64px;
    }
    .articles-container{
      display: flex;
      flex-wrap: wrap;
      gap: 30px;
      margin-bottom: 30px;
    }
    a{
      display: block;
      width: 100%;
      text-align: center;
      text-transform: uppercase;
      text-decoration: underline;
      font-size: 13px;
      font-weight: bold;
      text-underline-offset: 7px;
      margin-bottom: 147px;
    }
  }
}
</style>