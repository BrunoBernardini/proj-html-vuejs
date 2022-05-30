<template>
  <button>
    <a :href="buttonInfo.href">
      {{buttonInfo.name}} <i v-if="buttonInfo.arrow" class="fa-solid fa-arrow-right-long"></i>
    </a>
  </button>
</template>

<script>
export default {
  name: "ButtonComp",
  props: {
    buttonInfo: Object,
  }
}
</script>

<style lang="scss" scoped>
button{
  background-color: #20ac97;
  transition: all .15s;
  border: none;
  font-weight: bold;
  font-size: 13px;
  padding: 16px 58.5px;
  border-radius: 5px;
  a{
    color: white;
  }
  i{
    margin-left: 10px;
  }
  &:hover{
    background-color: #3f3a64;
  }
}
</style>