<template>
  <footer>
    <section class="container">
      <div class="left-half">
        <div class="footer-links">
          <h4>Address</h4>
          <ul>
            <li><a href="">382 NE 191st St # 87394 Miami, FL 33179-3899</a></li>
            <li><a href="">+1 (305) 547-9909 (9am - 5pm EST, Monday - Friday)</a></li>
            <li><a href="">support@maxcoach.com</a></li>
          </ul>
        </div>
      </div>
      <div class="right-half"></div>
    </section>
  </footer>
</template>

<script>
export default {
  name: "FooterComp",
}
</script>

<style lang="scss" scoped>
footer{
  display: flex;
  min-height: 405px;
  background-color: #171520;
  padding-top: 68px;
  .left-half,
  .right-half{
    width: 50%;
  }
  .footer-links{
    h4{
      color: white;
      font-size: 17px;
      font-weight: bold;
      margin-bottom: 17px;
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
</style>