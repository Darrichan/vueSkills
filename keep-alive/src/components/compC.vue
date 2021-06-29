<template>
  <h1>组件C</h1>
</template>
<script>
export default {
  mounted () {
    console.log('组件C渲染');
  },
  destroyed () {
    console.log('组件C销毁');
  }
}
</script>
<style>

</style>
