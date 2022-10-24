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
        // 最小值与最大值的设置
        min:0,
        max:100
      },
      yAxis: {
        //隐藏y轴
        show: false,
        // 均分
        type: "category",
      },
      //系列
      series: [
        {
          type: "bar",
          data: [78],
          color:'pink',
          barWidth:12,
          color:'yellowgreen',
          //背景颜色
          showBackground:true,
          backgroundStyle:{
            color:'#eee'
          },

          //文本
          label:{
            show:true,
            // 改变文本内容
            formatter:'|',
            // 更改文本标签位置
            position:'right'
          }

          },
      ],
      //布局调试
      grid: {
        left: 0,
        top: 0,
        right: 0,
        bottom: 0,
      },
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