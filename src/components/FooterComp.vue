<template>
  <footer>
    <section class="container content">
      <div class="left-half">
        <div
          v-for="(leftHalfList, index) in footerInfo.lists.leftHalf"
          :key="`leftHalfList-${index}`"
          class="footer-links">
          <h4>{{leftHalfList.listTitle}}</h4>
          <ul>
            <li
              v-for="(listElement, index) in leftHalfList.listOptions"
              :key="`${leftHalfList.listTitle}-${index}`">
              <a :href="listElement.href">{{listElement.name}}</a></li>
          </ul>
        </div>
        <ul class="socials">
          <li v-for="(social, index) in footerInfo.socialClasses"
          :key="`socialsFooter-${index}`"><a :href="social.href"><i :class="social.name"></i></a></li>
        </ul>
      </div>
      <div class="right-half">
        <div
          v-for="(leftHalfList, index) in footerInfo.lists.rightHalf"
          :key="`leftHalfList-${index}`"
          class="footer-links">
          <h4>{{leftHalfList.listTitle}}</h4>
          <ul>
            <li
              v-for="(listElement, index) in leftHalfList.listOptions"
              :key="`${leftHalfList.listTitle}-${index}`">
              <a :href="listElement.href">{{listElement.name}}</a></li>
          </ul>
        </div>
      </div>
    </section>
    <span class="under-footer">&copy; 2020 Maxcoach. All rights Reserved</span>
    <a href="#" class="back-btn"><i class="fa-solid fa-arrow-up-long"></i></a>
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
  props: {
    footerInfo: Object,
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

footer{
  position: relative;
  min-height: 405px;
  background-color: #171520;
  .content{
    display: flex;
    padding-top: 66px;
    margin-bottom: 70px;
    .left-half,
    .right-half{
      width: 50%;
    }
    .right-half{
      display: flex;
    }
    a{
      color: #bbbcbd;
    }
    .footer-links{
      margin: 0 67px 30px 0;
      h4{
        color: white;
        font-size: 17px;
        font-weight: bold;
        height: 24px;
      }
      ul{
        font-size: 14px;
        li{
          display: block;
          margin: 14px 0 0px 0;
        }
      }
    }
    .socials a{
      font-size: 24px;
      margin-right: 31px;
    }
  }
  .under-footer{
    color: #bbbcbd;
    width: 100%;
    display: block;
    font-size: 14px;
    text-align: center;
  }
  .back-btn{
    position: absolute;
    bottom: 40px;
    right: 40px;
    width: 50px;
    height: 50px;
    border-radius: 50%;
    background-color: $main-color;
    color: white;
    display: flex;
    justify-content: center;
    align-items: center;
  }
}
</style>