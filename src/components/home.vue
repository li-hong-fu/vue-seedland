<template>
  <div class="home-container">
    <div class="home-background">
      <div class="background-Hgrid-box">
        <p
          v-for="index in 5" :key="index"
          class="background-Hgrid"
          :class="'' + index"
          v-show="visible"></p>
      </div>
      <div class="background-Vgrid-box">
        <p
          v-for="index in 7" :key="index"
          class="background-Vgrid"
          :class="'' + index"
          v-show="visible"></p>
      </div>
      <div class="background-cross-box">
        <p v-for="index in 17" :key="index" :class="'background-cross' + index">+</p>
      </div>
    </div>
    <header class="home-header">
      <div class="header-logo">
        <img src="@/assets/images/Logo.gif">
      </div>
      <nav class="header-nav">
        <ul class="nav-container" id="nav">
          <li><a href="#about">关于实地</a></li>
          <li><a href="#development">地产开发</a></li>
          <li><a href="#news">最新消息</a></li>
          <li><a href="#joinus">加入实地</a></li>
          <li><a href="#whistleblower">廉洁举报</a></li>
          <li><a href="#contact">联系我们</a></li>
        </ul>
      </nav>
    </header>
    <main class="home-mainer">
      <div class="mainer-content">
        <div class="mainer-title">
          <p>THE FUTURE</p>
          <p>IS HERE</p>
        </div>
        <p class="mainer-subtitle">未来•就在眼前</p>
      </div>
    </main>
    <footer class="home-footer">
      <div class="footer-mousescroll">
        <p>向下滚动</p>
        <p>SCROLL DOWN FOR MORE</p>
      </div>
      <span class="footer-scroll-btn">
        <span class="footer-mouse">
          <span></span>
        </span>
      </span>
    </footer>
  </div>
</template>

<script>
export default {
  data () {
    return {
      visible: true
    }
  },
  created () {
    this.visible = false
    setTimeout(() => {
      this.visible = true
    }, 2000)
  }
}
</script>

<style lang="less" scoped>
.home-container{
  height: 100%;
  position: relative;
  display: flex;
  flex-direction: column;
  .home-background{
    position: absolute;
    width: 100%;
    height: 75%;
    top: 100px;
    left: 0;
    .background-Hgrid-box{
      @keyframes hgrid-1{
        0%{
          left: 50%;
          right: 50%;
          width: 0;
        }
        100%{
          left: 0;
          right: 0;
          width: 100%;
        }
      }
      @keyframes hgrid-2{
        0%{
          left: 37.5%;
          right: 62.5%;
          width: 0;
        }
        100%{
          left: 0;
          right: 0;
          width: 100%;
        }
      }
      @keyframes hgrid-3{
        0%{
          left: 75%;
          right: 25%;
          width: 0;
        }
        100%{
          left: 0;
          right: 0;
          width: 100%;
        }
      }
      @keyframes hgrid-4{
        0%{
          width: 0;
        }
        100%{
          left: 0;
          right: 0;
          width: 100%;
        }
      }
      position: relative;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      flex-direction: column;
      justify-content: space-between;
      opacity: 0.5;
      .background-Hgrid{
        width: 100%;
        background: #fff;
      }
      p:first-child{
        position: absolute;
        border-bottom: 3px solid transparent;
        animation: hgrid-1 3s linear 1;
      }
      p:last-child{
        position: absolute;
        bottom: 0;
        border-bottom: 3px solid transparent;
        animation: hgrid-1 3s linear 1;
      }
      p:nth-child(2){
        position: absolute;
        top: 25%;
        border-bottom: 1px solid transparent;
        animation: hgrid-2 3s linear 1;
      }
      p:nth-child(3){
        position: absolute;
        top: 50%;
        border-bottom: 1px solid transparent;
        animation: hgrid-3 3s linear 1;
      }
      p:nth-child(4){
        position: absolute;
        top: 75%;
        border-bottom: 1px solid transparent;
        animation: hgrid-4 3s linear 1;
      }
    }
    .background-Vgrid-box{
      @keyframes vgrid-1{
        0%{
          top: 75%;
          bottom: 25%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-2{
        0%{
          top: 50%;
          bottom: 50%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-3{
        0%{
          top: 75%;
          bottom: 25%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-4{
        0%{
          top: 50%;
          bottom: 50%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-5{
        0%{
          top: 25%;
          bottom: 75%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-6{
        0%{
          top: 50%;
          bottom: 50%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      @keyframes vgrid-7{
        0%{
          top: 75%;
          bottom: 25%;
          height: 0%;
        }
        100%{
          top: 0;
          bottom: 0;
          height: 100%;
        }
      }
      position: relative;
      top: -100%;
      left: 0;
      width: 100%;
      height: 100%;
      display: flex;
      justify-content: space-evenly;
      opacity: 0.5;
      .background-Vgrid{
        width: 1px;
        height: 100%;
        background: #fff;
      }
      p:nth-child(1){
        position: absolute;
        left: 12.5%;
        animation: vgrid-1 3s linear 1;
      }
      p:nth-child(2){
        position: absolute;
        left: 25%;
        animation: vgrid-2 3s linear 1;
      }
      p:nth-child(3){
        position: absolute;
        left: 37.5%;
        animation: vgrid-3 3s linear 1;
      }
      p:nth-child(4){
        position: absolute;
        left: 50%;
        animation: vgrid-4 3s linear 1;
      }
      p:nth-child(5){
        position: absolute;
        right: 37.5%;
        animation: vgrid-5 3s linear 1;
      }
      p:nth-child(6){
        position: absolute;
        right: 25%;
        animation: vgrid-6 3s linear 1;
      }
      p:nth-child(7){
        position: absolute;
        right: 12.5%;
        animation: vgrid-7 3s linear 1;
      }
    }
    .background-cross-box{
      position: absolute;
      top: 0;
      left: 0;
      width: 100%;
      height: 100%;
      p{
        color: #fff;
        font-size: 21px;
      }
      .background-cross1 {
        top: 25%;
        left: 12.5%;
        transform: translate(-7px,-17px);
        position: absolute;
        margin: 0;
        padding: 0;
      }
      .background-cross2 {
        left: 12.5%;
        transform: translate(-7px,-17px);
        position: absolute;
        top: 75%;
      }
      .background-cross3 {
        top: 0%;
        left: 25%;
        transform: translate(-7px,-15px);
        position: absolute;
      }
      .background-cross4 {
        top: 50%;
        left: 25%;
        transform: translate(-7px,-16px);
        position: absolute;
      }
      .background-cross5 {
        top: 100%;
        left: 25%;
        transform: translate(-7px,-17px);
        position: absolute;
      }
      .background-cross6 {
        top: 0%;
        left: 50%;
        transform: translate(-6px,-15px);
        position: absolute;
      }
      .background-cross7 {
        top: 50%;
        left: 50%;
        transform: translate(-6px,-16px);
        position: absolute;
      }
      .background-cross8 {
        top: 100%;
        left: 50%;
        transform: translate(-6px,-16px);
        position: absolute;
      }
      .background-cross9 {
        top: 25%;
        right: 37%;
        transform: translate(-3px,-16px);
        position: absolute;
      }
      .background-cross10 {
        top: 75%;
        right: 37%;
        transform: translate(-3px,-16px);
        position: absolute;
      }
      .background-cross11 {
        top: 0%;
        right: 25%;
        transform: translate(7px,-15px);
        position: absolute;
      }
      .background-cross12 {
        top: 50%;
        right: 24.5%;
        transform: translate(-3px,-16px);
        position: absolute;
      }
      .background-cross13 {
        top: 100%;
        right: 25%;
        transform: translate(7px,-17px);
        position: absolute;
      }
      .background-cross14 {
        top: 25%;
        right: 12%;
        transform: translate(-3px,-16px);
        position: absolute;
      }
      .background-cross15 {
        top: 75%;
        right: 12%;
        transform: translate(-3px,-16px);
        position: absolute;
      }
      .background-cross16 {
        top: 75%;
        left: 37.5%;
        transform: translate(-7px,-16px);
        position: absolute;
      }
      .background-cross17 {
        top: 25%;
        left: 37.5%;
        transform: translate(-7px,-16px);
        position: absolute;
      }
    }
  }
  .home-header{
    height: 14%;
    display: flex;
    justify-content: space-between;
    padding: 35px 50px 0 65px;
    .header-logo{
      width: 270px;
      height: 25px;
      img{
        width: 100%;
      }
    }
    .header-nav{
      position: absolute;
      width: 50%;
      right: 10%;
      font-family: monospace;
      font-size: 18px;
      ul{
        display: flex;
        list-style: none;
        li{
          position: relative;
          width: 100px;
           &:hover{
            &:after{
              content: "";
              position: absolute;
              width: 100%;
              height: 3px;
              top: -20px;
              left: 0;
              background: #fff;
              transition: .3s opacity;
            }
          }
          a{
            text-decoration: none;
            color: white;
          }
        }
        .active {
          font-weight: 600;
          font-family: monospace;
          font-size: 18px;
        }
      }
    }
  }
  .home-mainer{
    flex: 1;
    color: #fff;
    min-height: 600px;
    .mainer-content{
      position: relative;
      height: 100%;
      .mainer-title{
        position: absolute;
        font-family: "DIN-Regular";
        font-size: 51px;
        letter-spacing: 8px;
        top: 25%;
        right: 29%;
        text-align: left;
      }
      .mainer-subtitle{
        font-family: "NotoSansCJKsc-Thin";
        font-size: 35px;
        font-weight: 100;
        position: absolute;
        top: 50%;
        right: 37.5%;
      }
    }
  }
  .home-footer{
    @keyframes ani-mouse{
      0%{
        opacity: 1;
        top: 29%;
      }
      15%{
        opacity: 1;
        top: 71%;
      }
      50%{
        opacity: 0;
        top: 71%;
      }
      100%{
        opacity: 0;
        top: 71%;
      }
    }
    height: 100px;
    position: relative;
    color: #fff;
    .footer-mousescroll{
      position: absolute;
      top: -123px;
      left: 0;
      right: 0;
      transform: translateY(2px);
      animation: fadeInDown 1s 7s linear forwards;
      p:first-child{
        font-family: monospace;
        font-size: 22px;
        opacity: 0.8;
        margin-bottom: 7px;
        font-weight: 600;
      }
      p:last-child{
        font-size: 14px;
        letter-spacing: 3px;
        text-transform: uppercase;
        font-family: 'Roboto', sans-serif;
        padding-bottom: 14px;
        display: inline-block;
        border-bottom: 2px dashed #fff;
      }
    }
    .footer-scroll-btn{
      position: absolute;
      left: 0;
      right: 0;
      bottom: 0;
      animation: fadeInDown 1s 7s linear forwards;
      .footer-mouse{
        position: relative;
        display: block;
        width: 30px;
        height: 55px;
        margin: 0 auto 30px;
        box-sizing: border-box;
        border: 2px solid white;
        border-radius: 15px;
        opacity: 0.8;
        &::before{
          content: "";
          position: absolute;
          width: 1px;
          height: 160px;
          background: rgba(255,255,255,0.6);
          top: 52px;
          left: 50%;
          transform: translatex(-50%);
        }
        span{
          position: absolute;
          left: 50%;
          width: 8px;
          height: 8px;
          margin: -4px 0 0 -4px;
          background: #fff;
          border-radius: 50%;
          animation: ani-mouse 2.5s linear infinite;
        }
        &::after{
          content: "+";
          position: absolute;
          top: 200px;
          left: 50%;
          animation-name: spin;
          animation-duration: 1000ms;
          animation-iteration-count: 1;
          animation-timing-function: linear;
          transform: translatex(-50%) rotate(45deg);
        }
      }
    }
  }
}
</style>
