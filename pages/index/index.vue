<template>
  <view class="content">
    <view>1.全局样式可以写在App.vue里面，page和component页面写 scoped</view>
    <view>2.</view>
    <view v-for="(item, index) in buttonInfo" :key="index">
      <button type="primary" size="mini" @click="onClickBtn(item.url)">{{ item.info }}</button>
    </view>
    <button @click="test" size="mini">设置tabbar的消息</button>
  </view>
</template>

<script>
export default {
  data() {
    return {
      title: 'Hello',
      buttonInfo: [
        { info: '组件中.native .sync修饰符作用', url: '/pages/native/native' },
        { info: 'h5和小程序跳转传值问题', url: '/pages/navigate/navigate?name=hongan' },
        { info: 'api函数设置导航栏', url: '/pages/navigatebar/navigatebar' },
        { info: 'tapbar设置(包括iconfont)', url: '/pages/iconfontuse/iconfontuse' },
        {
          info: '--status-bar-height --window-top --window-bottom 等css变量使用方法',
          url: '/pages/css_global_value/css_global_value'
        }
      ]
    }
  },
  onLoad() {},
  methods: {
    onClickBtn(url) {
      uni.navigateTo({
        url
      })
    },
    test() {
      console.log(1111)
      uni.setTabBarBadge({
        index: 0,
        text: '10'
      })
    }
  }
}
</script>

<style scoped>
.content {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
}
</style>
