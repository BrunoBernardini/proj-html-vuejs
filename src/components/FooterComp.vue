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
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
  props: {
    footerInfo: Object
  }
}
</script>

<style lang="scss" scoped>
footer{
  background-color: #171520;
  .content{
    display: flex;
    min-height: 405px;
    padding-top: 66px;
    .left-half,
    .right-half{
      display: flex;
      width: 50%;
    }
    .footer-links{
      margin-right: 67px;
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
        a{
          color: #bbbcbd;
        }
      }
    }
  }
}
</style>