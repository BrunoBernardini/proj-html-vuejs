<template>
  <section class="yt-video">
    <div class="yt-thumb">
      <img :src="getImgUrl(videoInfo.img)" alt="Video">
      <a
        :href="videoInfo.href"
        class="yt-logo">
        <img src="../assets/img/icon-youtube-play.png" alt="YT Logo">
      </a>
    </div>

    <div class="yt-description">
      <h4 class="title">"{{videoInfo.description}}"</h4>
      <img class="wavy-separator" src="../assets/img/home-movation-shape-01.png" alt="Wavy line">
      <h5>{{videoInfo.personName}}</h5>
      <p>{{videoInfo.personRole.toUpperCase()}}</p>
    </div>
  </section>
</template>

<script>
export default {
  name: "YoutubeVideoSection",
  props: {
    videoInfo: Object,
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

.yt-video{
  display: flex;
  margin-bottom: 159px;
  .yt-thumb{
    flex-shrink: 0;
    position: relative;
    border-radius: 5px;
    overflow: hidden;
    height: max-content;
    box-shadow: 0 5px 16px 1px lightgray;
    .yt-logo{
      position: absolute;
      top: 50%;
      left: 50%;
      transform: translate(-50%, -50%);
      transition: all .15s;
      &:hover{
        transform: translate(-50%, -50%) scale(1.2);
      }
    }
  }
  .yt-description{
    padding: 57px 85px 0;
    h4{
      line-height: 45px;
      margin-bottom: 55px;
    }
    .wavy-separator{
      margin-bottom: 25px;
    }
    h5{
      color: $secondary-color;
      margin-bottom: 12px;
    }
    p{
      font-size: 12px;
    }
  }
}
</style>