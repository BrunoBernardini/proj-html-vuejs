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
          booksCards: [
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
          ],
          bookMenuOptions: [
            {
              name: "fa-solid fa-magnifying-glass",
              href: "#"
            },
            {
              name: "fa-solid fa-cart-shopping",
              href: "#"
            },
            {
              name: "fa-solid fa-heart",
              href: "#"
            },
            {
              name: "fa-solid fa-chart-column",
              href: "#"
            }
          ],
        },
        partnersInfo: [
          {
            img: "client-logo-05-primary.png",
            href: "#"
          },
          {
            img: "client-logo-06-primary.png",
            href: "#"
          },
          {
            img: "client-logo-07-primary.png",
            href: "#"
          },
          {
            img: "client-logo-04-primary.png",
            href: "#"
          },
          {
            img: "client-logo-03-primary.png",
            href: "#"
          },
          {
            img: "client-logo-02-primary.png",
            href: "#"
          }
        ],
        storiesInfo: [
          {
            story: "I am free to learn at my own pace, follow my own schedule and choose the subject I want to learn from the syllabus. Great study portal for people like me.",
            avatar: "testimonial-avata-02.jpg",
            name: "Mina Hollace",
            job: "/ Freelancer"
          },
          {
            story: "It has been an incredibly amazing experience! I could learn a lot of new things that changed my life forever, now I'm much more satisfied than before.",
            avatar: "testimonial-avata-01.jpg",
            name: "Hed Sciran",
            job: "/ Manager"
          },
          {
            story: "This has been exactly all I wanted, couldn't ask anything better. I'do re-do it again immediately!",
            avatar: "testimonial-avata-03.jpg",
            name: "Steven Job",
            job: "/ Employee"
          },
          {
            story: "Vi prego liberatemi non volevo fare una recensione positiva e loro mi hanno imprigionato!! E' una trappola, aiutoooo!",
            avatar: "testimonial-avata-04.jpg",
            name: "Franco Franchi",
            job: "/ Schiavo"
          },
        ],
        articlesInfo: {
          articleCards: [
            {
              img: "motivation-blog-04-480x325.jpg",
              date: {
                month: "May",
                day: 13,
                year: 2020
              },
              title: "How to Stay True to Your Personal Brand",
              synopsis: "When it comes to your business or career, you want"
            },
            {
              img: "motivation-blog-03-480x325.jpg",
              date: {
                month: "May",
                day: 13,
                year: 2020
              },
              title: "5 Vital Lessons in 5 Years of Freelancing",
              synopsis: "Being self-employed and working from home, it's easy to get"
            },
            {
              img: "motivation-blog-02-480x325.jpg",
              date: {
                month: "May",
                day: 13,
                year: 2020
              },
              title: "11 Super Useful Tips for Small-Business Owners",
              synopsis: "Being a small-business owner poses a ton of challenges. We"
            },
            {
              img: "motivation-blog-01-480x325.jpg",
              date: {
                month: "May",
                day: 13,
                year: 2020
              },
              title: "How to Give Yourself Grace to Start Again",
              synopsis: "Forgive yourself for bad habits you may have started or"
            },
          ],
          viewMoreHref: "#"
        }, 
      },
      footerInfo: {
        
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
