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
        },
        coursesInfo: {
          coursesCards: [
            {
              img: "motivation-course-06-480x298.jpg",
              price: 30,
              title: "How to be Successful: Create A Growth Mindset For Success",
              lessons: 3,
              students: 50
            },
            {
              img: "motivation-course-05-480x298.jpg",
              price: 30,
              title: "How to Build Confidence in Your Abilities",
              lessons: 1,
              students: 50
            },
            {
              img: "motivation-course-04-480x298.jpg",
              price: 20,
              title: "Productivity Machine - Focus in a Distracted World",
              lessons: 5,
              students: 50
            },
            {
              img: "motivation-course-03-480x298.jpg",
              price: 20,
              title: "Effective Time Management Mastery - Complete Guide",
              lessons: 18,
              students: 50
            },
            {
              img: "motivation-course-02-480x298.jpg",
              price: 25.99,
              title: "Body Language Secrets for Entrepreneurs",
              lessons: 19,
              students: 50
            },
            {
              img: "motivation-course-01-480x298.jpg",
              price: 19.99,
              title: "Management Skills: The Science of Leadership",
              lessons: 17,
              students: 50
            }
          ],
          buttonInfo: {
            name: "View all courses",
            href: "#",
            arrow: true
          }
        },
        booksInfo: {
          checkList: [
            "Help you understand yourself better",
            "Revealing mature tips",
            "Give the right advice",
            "Fascinating examples of alpha man"
          ],
          buttonInfo: {
            name: "Get Free Ebook",
            href: "#",
            arrow: false
          },
          booksCard: [
            {
              img: "product-book-11-400x400.jpg",
              href: "#",
              title: "Alpha man",
              author: "Maxcoach",
              price: 29
            },
            {
              img: "product-book-10-400x400.jpg",
              href: "#",
              title: "Real man 4.0",
              author: "Maxcoach",
              price: 39
            }
          ]
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
