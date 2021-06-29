<template>
  <h1>组件A</h1>
</template>
<script>
export default {
  mounted () {
    console.log('组件A渲染');
  },
  destroyed () {
    console.log('组件A销毁');
  }
}
</script>
<style>
</style>
