<template>
  <div id="app">
    <Background />
    <div class="header-side-nav">
      <button @click="value1 = true" type="primary">
        <img src="@/assets/images/hamburger.png">
      </button>
      <Drawer :closable="false" v-model="value1" width="400px">
        <ul id="menu" class="menu-container">
          <li>
            <a href="#home">
              <span>01</span><br><span>主页<br>HOME</span>
            </a>
          </li>
          <li>
            <a href="#about">
              <span>02</span><br><span>关于实地<br>ABOUT</span>
            </a>
          </li>
          <li>
            <a href="#development">
              <span>03</span><br><span>地产开发<br>DEVELOPMENT</span>
            </a>
          </li>
          <li>
            <a href="#news">
              <span>04</span><br><span>最新消息<br>LAST NEWS</span>
            </a>
          </li>
          <li>
            <a href="#joinus">
              <span>05</span><br><span>加入实地<br>JOIN US</span>
            </a>
          </li>
          <li>
            <a href="#whistleblower">
              <span>06</span><br><span>廉洁举报<br>WHISTLEBLOWER</span>
            </a>
          </li>
            <li>
            <a href="#contact">
              <span>07</span><br><span>联系我们<br>CONTACT</span>
            </a>
          </li>
        </ul>
      </Drawer>
    </div>
    <full-page
      class="fullpage-container"
      ref="fullpage"
      :options="options"
      id="fullpage">
      <div class="section home"><Home /></div>
      <div class="section about"><About /></div>
      <div class="section development"><Development /></div>
      <div class="section news"><News /></div>
      <div class="section joinus"><Joinus /></div>
      <div class="section whistleblower"><Whistleblower /></div>
      <div class="section contact"><Contact /></div>
    </full-page>
  </div>
</template>

<script type="text/javascript">
import Background from '@/components/Background.vue'
import Home from '@/components/home.vue'
import About from '@/components/About.vue'
import Development from '@/components/Development.vue'
import News from '@/components/News.vue'
import Joinus from '@/components/Joinus.vue'
import Whistleblower from '@/components/Whistleblower.vue'
import Contact from '@/components/Contact.vue'

export default {
  data () {
    return {
      value1: false,
      options: {
        licenseKey: '4F375E3E-7D814D7F-B82954BA-31DC667F',
        anchors: [
          'home',
          'about',
          'development',
          'news',
          'joinus',
          'whistleblower',
          'contact'
        ]
      }
    }
  },
  components: {
    Background,
    Home,
    About,
    Development,
    News,
    Joinus,
    Whistleblower,
    Contact
  }
}
</script>

<style lang="less">
.ivu-drawer-mask{
  width: 0;
}
.ivu-drawer-wrap{
  opacity: 0.6;
  .ivu-drawer-body{
    background: #000000;
    ul{
      list-style: none;
      padding-top: 50px;
      li{
        height: 68px;
        margin-bottom: 10px;
        a{
          display: flex;
          width: 100%;
          color: #fff;
          span{
            font-size: 18px;
            font-family: monospace;
          }
          span:first-child{
            width: 10%;
            float: left;
            padding-top: 10px;
          }
          span:last-child{
            padding: 0 0 10px 15px;
            border-left: 1px solid hsla(0,0%,100%,.41);
          }
        }
      }
    }
  }
}

.header-side-nav{
  position: fixed;
  right: 25px;
  top: 35px;
  z-index: 100;
  button{
    background: none;
    border: none;
    img{
      width: 25px;
    }
  }
}
.section{
  height: 100%;
}
</style>
