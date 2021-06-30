<template>
  <div id="app">
    <div>
      <button @click="percentClick"
              height="100%">开始</button>
      尺寸大小：
      <input v-model.number="circleSize"
             placeholder="circleSize"
             height="100%">
      {{msg}}
    </div>

    <progressCircle :circleSize="circleSize"
                    :percent="percent"></progressCircle>
  </div>
</template>

<script>
import progressCircle from './components/progress-circle.vue'
export default {
  data () {
    return {
      percent: 0,
      circleSize: 300,
      msg: '等待开启……'
    }
  },
  name: 'App',
  components: {
    progressCircle
  },
  methods: {
    percentClick () {
      for (let i = 0; i <= 10000; i++) {
        setTimeout(() => {
          this.percent = i * 0.0001;
        }, 50);
      }
      this.msg = '开启成功！'
    }
  }
}
</script>

<style>
</style>
