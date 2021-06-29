<template>
  <h1>组件B</h1>
</template>
<script>
export default {
  mounted () {
    console.log('组件B渲染');
  },
  destroyed () {
    console.log('组件B销毁');
  }
}
</script>
<style>

</style>
