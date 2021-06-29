<template>
  <div id="app">
    <div @click="handleClick">
      <ul>
        <li v-for="(item,index) in prj"
            :key="index"
            :dataIndex="index">{{item}}</li>
      </ul>
    </div>

  </div>
</template>

<script>
export default {
  data () {
    return {
      prj: ['项目1', '项目2', '项目3']
    }
  },
  name: 'App',
  methods: {
    handleClick (e) {
      console.log('index'+ e.target.getAttribute('dataindex'));
    }
  }
}
</script>

<style>
</style>
