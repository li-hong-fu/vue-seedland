<template>
  <div class="background-container">
    <div class="page-Spin" v-show="visible">
      <img src="@/assets/images/loading.gif" class="loading-img">
    </div>
    <div class="page-background">
      <video playsinline autoplay="autoplay" loop="loop" muted="muted" class="video">
        <source src="@/assets/videos/videobg.mp4" type="video/mp4">
      </video>
    </div>
  </div>
</template>

<script>
export default {
  data () {
    return {
      visible: false
    }
  },
  created () {
    this.visible = true
    setTimeout(() => {
      this.visible = false
    }, 1000)
  }
}
</script>

<style lang="less" scoped>
.page-Spin {
  position: fixed;
  top: 0;
  left: 0;
  z-index: 121;
  width: 100%;
  height: 100%;
  background: black;
  display: flex;
  align-items: center;
  justify-content: center;
  img {
  margin: 0 auto;
  width: 500px;
  z-index: 999;
  }
}
.page-background{
  width: 100%;
  max-height: 100%;
  height: 100%;
  overflow: hidden;
  position: fixed;
  top: 0;
  right: 0;
  z-index: -100;
}
</style>
