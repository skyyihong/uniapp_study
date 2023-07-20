<template>
  <view class="">
    <view class="">
      在Vue2中，默认自定义组件上的原生事件都是不起作用的，因为组件认为定义的事件都为自定义事件，如果使用原始事件需要加上修饰符.native
      ,vue3没有这个问题
    </view>
    <view>.sync 修饰符，是一个语法糖，实现在组件上 @update:mydata="mydata=$event"</view>
    <view>
      <testcpn :mydata.sync="mydata" @click.native="onclickCpn"></testcpn>
    </view>
  </view>
</template>

<script>
export default {
  data() {
    return {
      mydata: 'hongyan'
    }
  },
  methods: {
    onclickCpn() {
      console.log('onclickCpn')
    }
  }
}
</script>

<style lang="scss" scoped></style>
