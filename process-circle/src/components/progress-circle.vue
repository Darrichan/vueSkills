<template>
  <div class="process-circle">
    <svg :width="circleSize"
         :height="circleSize"
         viewBox="0 0 100 100">
      <circle r="50"
              cx="50"
              cy="50"
              fill="transparent"
              class="progress-background"></circle>
      <circle r="50"
              cx="50"
              cy="50"
              fill="transparent"
              class="progress-bar"
              :stroke-dasharray="dashArray"
              :stroke-dashoffset="dashOffset"></circle>
    </svg>
  </div>
</template>
<script>
export default {
  props: {
    circleSize: {
      type: Number,
      default: 100
    },
    percent:{
      type: Number,
      default:0
    }
  },
  data () {
    return {
      dashArray: Math.PI * 2 * 50
    }
  },
  computed: {
    dashOffset () {
      return (1 - this.percent) * this.dashArray;
    }
  }
}
</script>
<style>
circle {
  stroke-width: 10px;
  transform-origin: center;
  transform: scale(0.9);
}
.progress-background {
  stroke: rgba(66, 66, 66, 0.5);
}
.progress-bar {
  stroke: rgb(66, 66, 66);
  transform: rotate(-90deg) scale(0.9);
}
</style>
