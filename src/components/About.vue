<template>
  <swiper :options="swiperOption" ref="mySwiper" style="height: 100%;">
    <swiper-slide>
      <div class="swiper-title">
        <p>PROFILE</p>
        <p>项目简介</p>
      </div>
      <div class="swiper-profile">
        <div class="swiper-description">
          <p>Craftsmanship creates quality life products</p>
          <p>匠心筑就智慧人居精品</p>
        </div>
        <div class="swiper-simplebar">
          <simplebar data-simplebar-auto-hide="false">
            <span>
              <p>实地集团，2006年从广州出发，始于地产而不止于地产。13年来，实地一直致力于将人类科技的一切探索创新以人居业态为依托运用于生活中的方方面面，将科技与人文连接，重新构建人类对于自身与居住空间关系的认知。目前，实地集团已经发展成为一家为用户提供贯穿全生命周期智慧人居解决方案的综合性企业。</p>
              <p>实地集团现已覆盖全国六大最具成长力城市群，在26城全面绽放。每落子一地，均从区域先天资源的统筹观出发，开发每个城市的独特魅力，探索每个城市的人文价值，创造与之匹配的智能生活解决方案，为每座城市打造专属的人居经典。</p>
              <p>实地集团坚持用户至上原则，关注每一个个体的真实需求。从项目规划之初，就从用户痛点出发，以科技创新的产品思维先行，借助智能产品、数据分析、生活配套三位一体的服务体系，满足用户对居住环境安全、家庭健康、时间管理、情感交互等多维度的需求,以此为主线来逐步构建SLS (Smart Life System)智慧人居系统，为用户打造美好生活体验的同时，引领行业发展方向，提升城市整体的人居品质。</p>
            </span>
          </simplebar>
        </div>
      </div>
    </swiper-slide>
    <swiper-slide>
      <div class="swiper-title">
        <p>MILESTONES</p>
        <p>里程碑</p>
      </div>
      <div class="swiper-milestones">
        <simplebar data-simplebar-auto-hide="false">
          <span>
            <strong>萌芽，生长的开始</strong>
            <p>2006年,一股地产新兴势力在华南地区悄然崛起，实地集团正式成立。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
          <span>
            <strong>成熟，崭新的高度</strong>
            <p>2013年，实地集团发展日益成熟，战略触角延伸至华东等地区。实地•无锡玫瑰庄园等项目的落地标志着实地集团吹响进发中国东部房地产市场的号角，并向更高的目标迈进。</p>
          </span>
        </simplebar>
      </div>
    </swiper-slide>
    <swiper-slide>Slide 3</swiper-slide>
    <swiper-slide>Slide 4</swiper-slide>
    <swiper-slide>Slide 5</swiper-slide>
    <swiper-slide>Slide 6</swiper-slide>
    <div class="swiper-pagination swiper-pagination-white" slot="pagination"></div>
    <div class="swiper-button-prev swiper-button-white" slot="button-prev"></div>
    <div class="swiper-button-next swiper-button-white" slot="button-next"></div>
  </swiper>
</template>

<script>
import simplebar from 'simplebar-vue'
import 'simplebar/dist/simplebar.min.css'

export default {
  name: 'About',
  data () {
    return {
      swiperOption: {
        pagination: {
          el: '.swiper-pagination',
          clickable: true
        },
        navigation: {
          nextEl: '.swiper-button-next',
          prevEl: '.swiper-button-prev'
        }
      }
    }
  },
  components: {
    simplebar
  }
}
</script>

<style lang="less" scoped>
  ::-webkit-scrollbar {
    width: 4px;
    background-color: #7c849271;
    border-radius: 20px;
  }
  ::-webkit-scrollbar-thumb {
    background-color: white;
    border-radius: 20px;
  }
  ::-webkit-scrollbar-thumb:hover {
    background-color: white;
  }
  ::-webkit-scrollbar-thumb:active {
    border: 0;
    border-radius: 20px;
    background-color:white;
    height: 10px;
  }
  ::-webkit-scrollbar-thumb:window-inactive {
    background-color: white;
  }
  .swiper-container {
    height: 100%;
    position: relative;
    background: #000;
    opacity: 0.5;
    .swiper-wrapper{
      .swiper-slide {
        height: 100%;
        color: #FFF;
        .swiper-title{
          font-size: 18px;
          font-family: monospace;
          text-align: left;
          position: absolute;
          top: 5%;
          left: 5%;
          letter-spacing: 3px;
        }
        .swiper-profile{
          display: inline-block;
          width: 70vw;
          .swiper-description{
            position: absolute;
            font-size: 48px;
            font-family: "NotoSansCJKsc-Light", sans-serif;
            top: 15%;
            font-weight: 100;
            text-align: left;
          }
          .swiper-simplebar{
            position: absolute;
            right: 20%;
            top: 35%;
            width: 65vw;
            height: 25vh;
            font-family: monospace;
            font-size: 20px;
            text-align: left;
            overflow: auto;
            p{
              margin: 20px 0;
            }
          }
        }
        .swiper-milestones{
          font-family: "NotoSansCJKsc-Thin", sans-serif;
          font-size: 18px;
          text-align: left;
          height: 40vh;
          width: 75vw;
          max-width: 100%;
          overflow: auto;
          position: absolute;
          top: 30%;
          left: 15%;
          p{
            margin: 20px 0;
            font-weight: 100;
          }
        }
      }
    }
    .swiper-pagination{
      /deep/.swiper-pagination-bullet{
        height: 3px;
        width: 35px;
        background: #FFF;
        border-radius: 0%;
        margin-bottom: 5px;
      }
    }
  }
</style>
