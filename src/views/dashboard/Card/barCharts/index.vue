<template>
  <div class="charts" ref="charts"></div>
</template>


<!-- <script src="<script src="https://cdn.bootcdn.net/ajax/libs/echarts/5.3.3/echarts.common.js"></script>"></script> -->
<script>
import echarts from "echarts";
export default {
  mounted() {
    let lineCharts = echarts.init(this.$refs.charts);
    // 配置数据
    lineCharts.setOption({
      xAxis: {
        //隐藏x轴
        show: false,
        type: "category",
      },
      yAxis: {
        //隐藏y轴
        show: false,
      },
      //系列
      series: [
        {
          type: "bar",
          data: [30,40,10,20,30,40,20,30,10,20,30,30],
          color:'pink'
          },
      ],
      //布局调试
      grid: {
        left: 0,
        top: 0,
        right: 0,
        bottom: 0,
      },
      tooltip:{}
    });
  },
};
</script>

<style>
.charts {
  width: 100%;
  height: 100%;
}
</style>