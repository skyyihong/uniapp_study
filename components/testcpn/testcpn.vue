<template>
  <view @click="cpnClick">my-testcpn:{{ mydata }}</view>
</template>

<script>
export default {
  name: 'testcpn',
  props: {
    mydata: {
      type: String,
      default: 'hello word'
    }
  },
  data() {
    return {}
  },
  methods: {
    cpnClick() {
      this.$emit('update:mydata', 'kobe')
    }
  }
}
</script>

<style lang="scss" scoped>
view {
  background-color: red;
}
</style>
