# #任务：Vue 实地集团官网

随着 Vue 技术的普及大家用得趁手，而且组件能使自己的积累跟好的复用、迁移、和管理。越来越多的企业首页从开始使用 Vue 技术来构建。在本次任务中，我们使用 Vue 来为房地产企业开发一个传统的企业官网。

![image.png](https://cdn.nlark.com/yuque/0/2019/png/166094/1568943788742-39f5b9a6-ccaa-4342-9631-c1c86cdab150.png#align=left&display=inline&height=823&name=image.png&originHeight=1646&originWidth=3354&size=3903121&status=done&style=none&width=1677)

参考实地集团官网：[http://www.seedland.cc/](http://www.seedland.cc/)<br />在本地任务中你可以使用以下插件：

- 全屏滚动 fullPage：[https://alvarotrigo.com/fullPage/zh/](https://alvarotrigo.com/fullPage/zh/)
- fullpage.js 中文文档: [https://github.com/alvarotrigo/fullPage.js/tree/master/lang/chinese#fullpagejs](https://github.com/alvarotrigo/fullPage.js/tree/master/lang/chinese#fullpagejs)
- 全屏滚动 fullPage 的 Vue 版本：[https://github.com/alvarotrigo/vue-fullpage.js](https://github.com/alvarotrigo/vue-fullpage.js)
- 美化滚动条 [https://grsmto.github.io/simplebar/](https://grsmto.github.io/simplebar/)
- 轮播 [https://surmon-china.github.io/vue-awesome-swiper/](https://surmon-china.github.io/vue-awesome-swiper/)

> 市面上的很多插件大多基于原生和jQuery 开发，如果需要在 vue 中使用需要配置转一次，也可以寻找其 vue 版本的 vue 插件，例如 fullPage.js 的有 vue-fullpage.js


任务要求：

- 完成 实地集团 首页的全屏滚动展示效果即可。（ 详情页不作要求，有时间自己折腾 ）

任务提示：

- 使用 Vue-cli 构建
- 首屏幕展示的 Loading 效果为 Gif 图片 [http://www.seedland.cc/wp/wp-content/themes/Seedland/assets/images/preloader.gif](http://www.seedland.cc/wp/wp-content/themes/Seedland/assets/images/preloader.gif) ，开始展示当背景视频加载完毕时候消失展示主体内容。（ 选做 )
- 背景视频地址为 [http://www.seedland.cc/assets/videos/videobg.mp4](http://www.seedland.cc/assets/videos/videobg.mp4) 可参考抖音的实现效果。（ 最好下载到本地然后上传到自己的七牛 CDN 来使用 )
- fullpage.js 为商业插件需要收费，不推荐偷别人家的码例如 licenseKey: '4F375E3E-7D814D7F-B82954BA-31DC667F'

代码示例：

1. cd ~/Desktop && vue create seedland-vue
1. npm install vue-fullpage.js -S
1. npm install simplebar-vue -S
1. npm install vue-awesome-swiper -S
1. Vue 注册
```javascript
import Vue from "vue";
import App from "./App.vue";
import router from "./router";
// 全屏滚动
import VueFullPage from "vue-fullpage.js";
// 轮播图
import VueAwesomeSwiper from "vue-awesome-swiper";
import "swiper/dist/css/swiper.css";

Vue.config.productionTip = false;
Vue.use(VueFullPage);
Vue.use(VueAwesomeSwiper);

new Vue({
  router,
  render: h => h(App)
}).$mount("#app");

```

4. 在组件中使用
```html
<template>
  <div id="app">
    <ul id="menu" class="menu-container">
      <li><a data-menuanchor="about" href="#about">关于实地</a></li>
      <li><a data-menuanchor="development" href="#development">地产开发</a></li>
      <li><a data-menuanchor="news" href="#news">最新消息</a></li>
      <li><a data-menuanchor="joinus" href="#joinus">加入实地</a></li>
      <li>
        <a data-menuanchor="whistleblower" href="#whistleblower">廉洁举报</a>
      </li>
      <li><a data-menuanchor="contact" href="#contact">联系我们</a></li>
    </ul>

    <full-page
      class="fullpage-container"
      ref="fullpage"
      :options="options"
      id="fullpage"
    >
      <div class="section">未来•就在眼前</div>
      <div class="section">
        <swiper :options="swiperOption" ref="mySwiper" style="height: 100%;">
          <!-- slides -->
          <swiper-slide>关于实地 1</swiper-slide>
          <swiper-slide>关于实地 2</swiper-slide>
          <swiper-slide>关于实地 3</swiper-slide>
          <swiper-slide>关于实地 4</swiper-slide>
          <swiper-slide>关于实地 5</swiper-slide>
          <swiper-slide>关于实地 6</swiper-slide>
          <!-- Optional controls -->
          <div class="swiper-pagination" slot="pagination"></div>
          <div class="swiper-button-prev" slot="button-prev"></div>
          <div class="swiper-button-next" slot="button-next"></div>
        </swiper>
      </div>
      <div class="section">
        <simplebar data-simplebar-auto-hide="false">
          <div class="flex-cell">
            <div class="flex-cell-card" style="background-color: #333;"></div>
            <div class="flex-cell-card" style="background-color: #444;"></div>
            <div class="flex-cell-card" style="background-color: #555;"></div>
            <div class="flex-cell-card" style="background-color: #666;"></div>
            <div class="flex-cell-card" style="background-color: #777;"></div>
            <div class="flex-cell-card" style="background-color: #888;"></div>
            <div class="flex-cell-card" style="background-color: #999;"></div>
            <div class="flex-cell-card" style="background-color: #000;"></div>
            <div class="flex-cell-card" style="background-color: #111;"></div>
            <div class="flex-cell-card" style="background-color: #222;"></div>
            <div class="flex-cell-card" style="background-color: #333;"></div>
            <div class="flex-cell-card" style="background-color: #444;"></div>
          </div>
        </simplebar>
      </div>
      <div class="section">最新消息</div>
      <div class="section">加入实地</div>
      <div class="section">廉洁举报</div>
      <div class="section">联系我们</div>
    </full-page>
  </div>
</template>

<script type="text/javascript">
import simplebar from 'simplebar-vue';
import 'simplebar/dist/simplebar.min.css';
export default {
  data() {
    return {
      options: {
        licenseKey: "4F375E3E-7D814D7F-B82954BA-31DC667F",
        menu: "#menu",
        anchors: [
          "landing",
          "about",
          "development",
          "news",
          "joinus",
          "whistleblower",
          "contact"
        ],
        sectionsColor: [
          "#41b883",
          "#ff5f45",
          "#0798ec",
          "rgba(0,0,0,.2)",
          "rgba(0,0,0,.4)",
          "rgba(0,0,0,.6)",
          "rgba(0,0,0,.8)"
        ]
      },
      swiperOption: {
        loop: true,
        pagination: {
          el: ".swiper-pagination",
          clickable: true
        },
        navigation: {
          nextEl: ".swiper-button-next",
          prevEl: ".swiper-button-prev"
        }
      }
    };
  },
  components: {
    simplebar
  }
};
</script>

<style lang="less">
body {
  padding: 0;
  margin: 0;
}
.menu-container {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 2;

  .active {
    background-color: #35b558;
  }
}

.flex-cell{
  display: flex;
  width: 2400px;
  height: 100vh;
  flex-wrap: wrap;
  .flex-cell-card{
    flex:none;
    background: #333;
    width: 400px;
    height: 50%;
  }
}
</style>
```

