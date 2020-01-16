<template>
  <div class="newsbox">
    <div class="news-title">
      <span class="secondary-title">最新消息</span>
      <span class="main-title">LATEST NEWS</span>
    </div>
    <div class="exploremore">
      <div class="left">
        <span>FIND OUT MORE</span>
        <span>了解更多</span>
      </div>
      <div class="right">
        <i></i>
        <i></i>
      </div>
      <i class="upperLeft">+</i>
      <i class="upperRight">+</i>
      <i class="leftLower">+</i>
      <i class="lowRight">+</i>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {}
  }
}
</script>

<style lang="less" scoped>
 .newsbox{
  height: 100%;
  position: relative;
  background-color: rgba(0,0,0,.24);
  .news-title{
    position: absolute;
    left: 50%;
    top: 50%;
    transform: translateY(-50%);
    margin-top: 3%;
    padding-top: 100px;
    padding-left: 5%;
    padding-right: 5%;
    display: flex;
    flex-direction: column;
    text-align: left;
    min-width: 584px;
    .secondary-title{
      font-size: 44px;
      font-family: NotoSansCJKsc-Light;
      font-weight: lighter;
      color: #ffffff;
    }
    .main-title{
      font-size: 65px;
      font-weight: lighter;
      text-transform: uppercase;
      font-family: NotoSansCJKsc-Thin;
      color: #ffffff;
    }
  }
  .exploremore{
    position: absolute;
    right: 6vw;
    bottom: 7vh;
    background-color: transparent;
    border: 1px solid #fafafa;
    padding: 8px 13px;
    margin-right: 0;
    width: 350px;
    color: #fff;
    cursor: pointer;
    .left{
      display: flex;
      flex-direction: column;
      text-align: left;
      float: left;
      font-size: 18px;
      font-family: monospace;
    }
    .right{
      float: right;
      i:first-child{
        border-bottom: 2px solid #fafafa;
        margin-top: 25px;
        position: absolute;
        width: 70px;
        right: 60px;
        top: 0;
      }
      i:last-child{
        border-bottom: 2px solid #fafafa;
        margin-top: 1px;
        position: absolute;
        width: 12px;
        transform: rotate(32deg);
        transform-origin: bottom right;
        right: 60px;
        top: 24px;
      }
    }
    .upperLeft{
      position: absolute;
      top: -13px;
      left: -7px;
      font-size: 18px;
    }
    .upperRight{
      position: absolute;
      top: -13px;
      right: -5px;
      font-size: 18px;
    }
    .leftLower{
      position: absolute;
      bottom: -15px;
      left: -7px;
      font-size: 18px;
    }
    .lowRight{
      position: absolute;
      bottom: -15px;
      right: -5px;
      font-size: 18px;
    }
  }
 }
</style>
