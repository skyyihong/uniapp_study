<template>
  <view class="">
    <view>1.小程序和h5可以用onload传值</view>
    <view>2.h5可以用 this.$router.query 进行传值</view>
  </view>
</template>

<script>
export default {
  inheritAttrs: true,
  props: ['name'],
  data() {
    return {}
  },
  methods: {},

  mounted() {
    console.log(this.$route.query)
  },
  onLoad(options) {
    console.log(options)
  }
}
</script>

<style scoped></style>
