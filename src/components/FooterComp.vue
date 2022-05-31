<template>
  <footer>
    <section class="container content">
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
      <div class="right-half">
        <div class="footer-links">
          <h4>Explore</h4>
          <ul>
            <li><a href="">Start here</a></li>
            <li><a href="">Blog</a></li>
            <li><a href="">About us</a></li>
          </ul>
        </div>
        <div class="footer-links">
          <h4></h4>
          <ul>
            <li><a href="">Success story</a></li>
            <li><a href="">Courses</a></li>
            <li><a href="">Contact us</a></li>
          </ul>
        </div>
        <div class="footer-links">
          <h4>Information</h4>
          <ul>
            <li><a href="">Membership</a></li>
            <li><a href="">Purchase guide</a></li>
            <li><a href="">Privacy policy</a></li>
            <li><a href="">Terms of service</a></li>
          </ul>
        </div>
      </div>
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