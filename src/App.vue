<template>
  <div id="app">
    <div>
      <span>Date range picker:</span>
      <date-picker v-model="filterDateRange" range width="220" placeholder="from ~ to"></date-picker>
    </div>
    <div>
      <span>filter: {{ filterText }}</span>
    </div>
  </div>
</template>

<script>
import DatePicker from 'vue2-datepicker'
import moment from 'moment-timezone'
import R from 'ramda'

export default {
  name: 'app',
  components: {
    DatePicker
  },
  data() {
    return {
      time1: '',
      filterDateRange: '',
    }
  },
  computed: {
    filterText() {
      console.log('filterDateRange = ', this.filterDateRange)
      let filters = {};
      if (!!this.filterDateRange && this.filterDateRange.length === 2) {
        filters['from_date'] = moment(this.filterDateRange[0]).tz('Asia/Singapore').format('YYYY-MM-DD');
        filters['to_date'] = moment(this.filterDateRange[1]).tz('Asia/Singapore').format('YYYY-MM-DD');
      }

      console.log('filters = ', filters)

      let filterTexts = [];
      const pushText = (value, column) => {
        filterTexts.push(column + '|' + value);
      }
      R.forEachObjIndexed(pushText, filters);
      const text = filterTexts.join(',');

      console.log('filterTexts = ', filterTexts, ', text = ', text);
      return text;
    }
  }
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
