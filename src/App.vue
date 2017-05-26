<template>
  <div id="app">
    <span>Date range picker:</span>
    <date-picker v-model="time2" range width="220" placeholder="from ~ to"></date-picker>
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker'

export default {
  name: 'app',
  components: {
    DatePicker
  },
  data() {
    return {
      time1: '',
      time2: '',
    }
  },
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
