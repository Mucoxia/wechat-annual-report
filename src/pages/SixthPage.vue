<template>
  <div class="column justify-center">
    <div class="text">似乎更喜欢在下班时分聊天，下午6点的聊天记录有1318条。</div>
    <div id="chart2" class="chart-container bg-white">
    </div>
  </div>
</template>

<script>
import ApexCharts from 'apexcharts'
export default {
  data() {
    return {
      chartOptions: {
        chart: {
          type: 'line'
        },
        series: [{
          name: '聊天数',
          data: [11, 7, 0, 0, 0, 3, 75, 730, 1068, 791, 815, 509, 563, 655, 913, 989, 1165, 1318, 879, 1050, 995, 509, 688, 384]
        }],
        xaxis: {
          categories: [1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11, 12, 13, 14, 15, 16, 17, 18, 19, 20, 21, 22, 23, 24]
        }
      }
    }
  },
  mounted() {
    const chart = new ApexCharts(document.querySelector("#chart2"), this.chartOptions);
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