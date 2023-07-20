<template>
  <view class="fix">
    --status-bar-height --window-top --window-bottom 是uniapp的css变量，可以在不同设备下获取不同的数值，
    <view class="">--status-bar-height ：是指信号、电池那个状态栏的高</view>
    <view>--window-top：是指信号+头顶标签栏的高</view>
    <view>--window-bottom:指去tabbar的高</view>
    <view class="bottom">底部</view>
  </view>
</template>

<script>
export default {
  data() {
    return {}
  },
  methods: {}
}
</script>

<style lang="scss" scoped>
.fix {
  position: fixed;
  top: var(--window-top);
  left: 0;
  background-color: red;
  z-index: 997;
  .bottom {
    width: 100vw;
    position: fixed;
    bottom: var(--window-bottom);
    left: 0;
    height: 100rpx;
    background-color: pink;
  }
}
</style>
