<template>
  <div class="article-card">
    <img
      :src="getImgUrl(articleInfo.img)"
      :alt="articleInfo.img">
    <p><i class="fa-regular fa-calendar"></i>{{`${articleInfo.date.month}, ${articleInfo.date.day} ${articleInfo.date.year}`}}</p>
    <h5>{{articleInfo.title}}</h5>
    <p class="synopsis">{{articleInfo.synopsis}}</p>
  </div>
</template>

<script>
export default {
  name: "ArticleCard",
  props:{
    articleInfo: Object
  },
  methods: {
    getImgUrl(img){
      return require("../assets/img/"+img);
    }
  }
}
</script>

<style lang="scss" scoped>
.article-card{
  width: 271px;
  border-radius: 5px;
  margin-bottom: 6px;
  transition: all .15s;
  img{
    border-radius: 5px;
    margin-bottom: 29px;
  }
  p{
    font-size: 14px;
    margin-bottom: 8px;
    line-height: 24px;
    i{
      margin-right: 6px;
    }
  }
  h5{
    font-weight: bold;
    line-height: 32px;
    margin-bottom: 17px;
  }
  .synopsis::after{
    content: " ...";
  }
  &:hover{
    box-shadow: 0 0 16px lightgray;
  }
}
</style>