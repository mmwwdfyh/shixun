<template>
  <div>
    <div id="main" style="width: 600px; height: 400px;"></div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
  created() {},
  mounted() {
      this.fyh();
  },
  methods: {
    fyh() {
      let myChart = this.$echarts.init(document.getElementById("main"));

      //指定图表的配置项和数据
      let option = {
        title: {
          text: "ECharts 入门市例"
        },
        tooltip: {},
        legend: {
          data: ["销量"]
        },
        xAxis: {
          data: ["衬衫", "羊毛衫", "仿山", "裤子", "高跟鞋", "袜子"]
        },
        yAxis: {},
        series: [
          {
            name: "销量",
            type: "bar",
            data: [5, 25, 36, 15, 10, 20]
          }
        ]
      };
      //使用刚指定的配置项和数据显示图表
      myChart.setOption(option);
    }
  }
};
</script>

<style scoped lang="less"></style>
