<template>
  <view>
    <view>导航栏和tabbar都可以通过命令进行设置</view>
    <button @click="setNavi">设置导航条</button>
  </view>
</template>

<script>
export default {
  methods: {
    setNavi() {
      console.log('setNavi')
      uni.setNavigationBarTitle({
        title: 'test'
      })
      uni.setNavigationBarColor({
        backgroundColor: '#00cc00',
        frontColor: '#ffffff'
      })
    }
  }
}
</script>

<style scoped lang="scss"></style>
