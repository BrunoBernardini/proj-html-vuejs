<template>
  <div class="course-card">
    <img
      :src="getImgUrl(courseInfo.img)"
      :alt="courseInfo.img">
    <div class="text-box">
      <h3 class="highlight">${{Math.floor(courseInfo.price)}}.<span class="cents">{{cents}}</span></h3>
      <h2>{{courseInfo.title}}</h2>
      <p>
        <span class="spec"><i class="fa-regular fa-file-lines"></i> {{courseInfo.lessons}} Lessons</span>
        <span class="spec"><i class="fa-regular fa-user"></i> {{courseInfo.students}} Students</span>
      </p>
    </div>
  </div>
</template>

<script>
export default {
  name: "CourseCard",
  props: {
    courseInfo: Object
  },
  methods: {
    getImgUrl(img){
      return require("../assets/img/"+img);
    }
  },
  computed: {
    cents(){
      let cents = Math.round((this.courseInfo.price - Math.floor(this.courseInfo.price))*100);
      if(cents !== 0) return cents;
      else return "00";
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

.course-card{
  width: 370px;
  border-radius: 5px;
  overflow: hidden;
  transition: all .15s;
  .text-box{
    text-align: start;
    width: 100%;
    padding: 26px 30px;
    h3{
      font-size: 24px;
      font-weight: bold;
      margin-bottom: 10px;
    }
    .cents{
      font-size: 17px;
    }
    h2{
      font-size: 19px;
      font-weight: bold;
      line-height: 32px;
      color: $secondary-color;
      margin-bottom: 32px;
    }
    p{
      font-size: 14px;
      i{
        margin-right: 6px;
      }
      .spec{
        display: inline-block;
        margin-right: 25px;
      }
    }
  }
  &:hover{
    box-shadow: 0 0 16px lightgray;
  }
}
</style>