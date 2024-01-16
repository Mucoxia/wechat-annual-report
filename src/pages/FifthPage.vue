<template>
  <div class="column justify-center">
    <div class="text">{{ `聊天最多的月份是${mostMonth}月份，有${count}条` }}</div>
    <div id="chart" class="chart-container bg-white">
    </div>
  </div>
</template>

<script>
import { monthData } from "../data.json";
import ApexCharts from 'apexcharts'
export default {
  data() {
    return {
      ...monthData,
      chartOptions: {
        chart: {
          type: 'line'
        },
        series: [{
          name: '聊天数',
          data: [1363, 1361, 1792, 826, 714, 1774, 1236, 1605, 2065, 1381]
        }],
        xaxis: {
          categories: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10]
        }
      }
    }
  },
  mounted() {
    const chart = new ApexCharts(document.querySelector("#chart"), this.chartOptions);
    chart.render()
  }
};
</script>
<style  lang="stylus" scoped>
.text{
  font-size: 4vw;
  font-weight: bolder;
}
.chart-container{
  margin-top:10vh;
  width:100%;
  height:30vh!important;
  opacity:0.7;
  border-radius:10px
}
</style>