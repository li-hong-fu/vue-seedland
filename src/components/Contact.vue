<template>
  <div class="contact-container">
    <div class="contact-body">
      <div class="left">
        <div class="select">
          <select v-model="optionsIndex" @change="site">
            <option v-for="(data, index) in options.title" :value="index" :key="index" >{{data}}</option>
          </select>
        </div>
        <div class="address">
          <span>{{options.address1[optionsIndex]}}</span><br>
          <span>{{options.address2[optionsIndex]}}</span>
        </div>
        <div class="phone">{{options.phone[optionsIndex]}}</div>
      </div>
      <nav class="right">
        <ul class="container" id="nav">
          <li><a href="#about">关于实地 ABOUT</a></li>
          <li><a href="#development">地产开发 DEVELOPMENT</a></li>
          <li><a href="#news">最新消息 LATEST NEWS</a></li>
          <li><a href="#joinus">加入实地 JOIN US</a></li>
          <li><a href="#whistleblower">廉洁举报 WHISTLEBLOWER</a></li>
        </ul>
      </nav>
    </div>
    <div class="contact-footer">
      <div class="contact-logo">
        <img src="@/assets/images/Logo.gif" alt="logo">
      </div>
      <div class="contact-info">
        <p>
          <span>友情链接:</span>
          <a href="">哈奇智能</a>
          <a href="">37度智能家居</a>
          <a href="">全球智慧生活创想者大奖</a>
        </p>
        <p>©2018 版权所有：实地地产集团有限公司</p>
        <p>ALL RIGHTS RESERVED: GUANGZHOU SEEDLAND REAL ESTATE DEVELOPMENT CO., LTD</p>
        <p>粤ICP备13058296号</p>
      </div>
      <div class="contact-go">
        <span>联系</span>
        <span>CONTACT</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      optionsIndex: 0,
      options: {
        title: [
          '实地集团(总部)',
          '广州蔷薇花园',
          '广州常春藤',
          '昆明花鹤翎',
          '深圳剑兰郡',
          '天津海棠雅著',
          '永川蔷薇国际',
          '惠州常春藤',
          '遵义蔷薇国际',
          '武汉君兰汀岸',
          '无锡玫瑰庄园',
          '中山璟湖城',
          '六盘水紫藤庄园',
          '三亚海棠华著',
          '黄冈蔷薇国际',
          '惠州木槿雅著',
          '太原紫藤公馆',
          '成都海棠名著',
          '周口九里香堤'
        ],
        address1: [
          '广州市天河区华夏路16号富力盈凯广场21楼',
          '广州广汕路21号线钟岗地铁站西侧',
          '广州市黄埔区乔丰路与永和大道交汇处',
          '昆明市北三环与普吉路交汇处',
          '深圳市罗湖区红桂路红桂横街27号',
          '津蓟高速温泉城出口西侧500米',
          '永川万达旁',
          '惠州市惠阳区惠南大道旁',
          '遵义市新蒲新区播州大道与新蒲大道交叉路口',
          '武汉汉阳经济技术开发区滨江带',
          '无锡市惠山区城铁国际商务区',
          '中山市火炬开发区博爱七路113号',
          '中山市火炬开发区博爱七路113号',
          '三亚海棠区海棠北路18号（海棠广场北侧200米）',
          '黄冈市黄州区黄冈大道西侧',
          '惠阳经济开发区御和路（淡水河岸）',
          '太原市晋阳街与体育路交汇处以南',
          '成都市青白江新城中心家乐福旁',
          '文昌大道与武盛大道交会处东1000米招商大厦北侧'
        ],
        address2: [
          '21st Floor, R&F Yingkai Plaza, 16 Huaxia Road, Tianhe District, Guangzhou'
        ],
        phone: [
          '020-89192000',
          '020-3263 6888',
          '020-2622 7888',
          '0871-64336666',
          '0755-22380888',
          '022-29208228',
          '023-49585888',
          '0752-3916888',
          '0852-8869999',
          '027-83769888',
          '0510-83256666',
          '0760-88588868',
          '0858-8325378',
          '0898-88859999',
          '0731-8888811',
          '0752-3737111',
          '0351-5658888',
          '028-83662666',
          '0394-8591111'
        ]
      }
    }
  },
  methods: {
    site: function (index) {
      console.log(this.optionsIndex)
    }
  }
}
</script>

<style lang="less" scoped>
  .contact-container{
    height: 100%;
    position: relative;
    .contact-body{
      display: flex;
      position: absolute;
      width: 100%;
      justify-content: space-between;
      padding: 0 65px;
      bottom: 15%;
      .left{
        text-align: left;
        .select{
          position: relative;
          &::after{
            content: url('../assets/images/contact.png');
            font: 35px Consolas,monospace;
            right: 18%;
            top: 25%;
            position: absolute;
          }
          select{
            -webkit-appearance: none;
            width: 100%;
            max-width: 350px;
            height: 50px;
            margin: 5px 0;
            padding: 0 24px;
            font-size: 16px;
            line-height: 1.75;
            color: #fff;
            background-color: transparent!important;
            border: 1px solid #ffffff;
            outline: none;
            option{
              background-color: #333!important;
            }
          }
        }
        .address{
          margin-top: 50px;
          color: #fff;
          span:first-child{
            width: 400px;
            font-size: 18px;
            font-family: monospace;
            display: block;
          }
          span:last-child{
            font-size: 12px;
          }
        }
        .phone{
          margin-top: 30px;
          font-size: 18px;
          color: #fff;
          font-family: monospace;
        }
      }
      .right{
        ul{
          padding-left: 10px;
          list-style: none;
          text-align: left;
          li{
            padding: 10px;
            font-size: 14px;
            a{
              color: #fff;
              text-decoration: none;
            }
          }
        }
      }
    }
    .contact-footer{
      display: flex;
      justify-content: space-between;
      align-items: center;
      position: absolute;
      bottom: 10px;
      width: 100%;
      padding: 0px 65px;
      color: #fff;
      .contact-logo{
        width: 18%;
        img{
          width: 100%;
        }
      }
      .contact-info{
        font-size: 14px;
        a{
          color: #fff;
          text-decoration: none;
          margin-left: 8px;
        }
      }
      .contact-go{
        width: 212px;
        text-align: right;
        font-size: 20px;
        letter-spacing: 4px;
        text-align: left;
        position: relative;
        cursor: pointer;
        &::after{
          content: url('../assets/images/contact.png');
          right: -5px;
          top: 0;
          position: absolute;
        }
        span{
          margin-right: 10px;
        }
      }
    }
  }
</style>
