<template>
  <div id="app">

    <button @click="state='A'">A</button>
    <button @click="state='B'">B</button>
    <button @click="state='C'">C</button>
    <!-- <keep-alive>
      <comp-a v-if="state==='A'"></comp-a>
      <comp-b v-if="state==='B'"></comp-b>
      <comp-c v-if="state==='C'"></comp-c>
    </keep-alive>

      <comp-a v-if="state==='A'"></comp-a>
      <comp-b v-if="state==='B'"></comp-b>
      <comp-c v-if="state==='C'"></comp-c> -->

    <comp-a v-show="state==='A'"></comp-a>
    <comp-b v-show="state==='B'"></comp-b>
    <comp-c v-show="state==='C'"></comp-c>

  </div>
</template>

<script>
import compA from './components/compA.vue'
import compB from './components/compB.vue'
import compC from './components/compC.vue'
export default {
  data () {
    return {
      state: 'null'
    }
  },
  name: 'App',
  components: {
    compA, compB, compC
  }
}
</script>

<style>
</style>
