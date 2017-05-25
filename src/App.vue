<template>
  <div id="app">
    <span>Try to add date picker here:</span>
    <!-- <date-picker v-model="time2" range></date-picker> -->
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker'

export default {
  name: 'app',
  components: {
    // DatePicker
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
