<template>
  <div class="book-card">
    <div class="book-img">
      <img
        :src="getImgUrl(bookInfo.img)"
        :alt="bookInfo.img">
      <div class="card-menu">
        <a 
          v-for="(bookMenuOption, index) in bookMenuOptions"
          :key="`bookMenuOption-${index}`"
          :href="bookMenuOption.href"
          class="menu-option"><i :class="bookMenuOption.name"></i>
        </a>
      </div>
    </div>
    <h3>{{bookInfo.title}} by {{bookInfo.author}}</h3>
    <h4 class="highlight">${{Math.floor(bookInfo.price)}}.<span class="cents">{{cents}}</span></h4>
  </div>
</template>

<script>
export default {
  name: "BookCard",
  props: {
    bookInfo: Object,
    bookMenuOptions: Array
  },
  methods: {
    getImgUrl(img){
      return require("../assets/img/"+img);
    }
  },
  computed: {
    cents(){
      let cents = Math.round((this.bookInfo.price - Math.floor(this.bookInfo.price))*100);
      if(cents !== 0) return cents;
      else return "00";
    }
  }
}
</script>

<style lang="scss" scoped>
@import "../assets/style/vars";

.book-card{
  width: 328px;
  text-align: center;
  .book-img{
    position: relative;
    margin-bottom: 21px;
    overflow: hidden;
    img{
      transition: all .15s;
    }
    &:hover img{
      scale: 1.1;
    }
    .card-menu{
      display: flex;
      flex-direction: column;
      gap: 14px;
      position: absolute;
      right: 33px;
      top: 50%;
      transform: translateY(-50%);
      opacity: 0;
      transition: all .15s;
      .menu-option{
        cursor: pointer;
        position: relative;
        width: 37px;
        height: 37px;
        border-radius: 50%;
        color: black;
        background-color: white;
        box-shadow: 1px 1px 5px lightgray;
        transition: all .15s;
        &:hover{
          background-color: lightgray;
        }
        i{
          position: absolute;
          top: 50%;
          left: 50%;
          transform: translate(-50%, -50%);
        }
      }
    }
    &:hover .card-menu{
      opacity: 1;
    }
  }
  h3{
    font-size: 19px;
    font-weight: bold;
    line-height: 32px;
    color: $secondary-color;
    margin-bottom: 8px;
  }
  h4{
    font-size: 24px;
    font-weight: bold;
    margin-bottom: 10px;
  }
  .cents{
    font-size: 17px;
  }
}
</style>