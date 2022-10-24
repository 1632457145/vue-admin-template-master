<template>
  <div>
    <el-row :gutter="10">
      <el-col :span="6">
        <el-card>
          <!-- 第一个card -->
          <detail title="总销售额" count="￥ 126560">
            <template slot="charts">
              <span>周同比 56.67%  <svg t="1663060529876" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6308" width="16" height="16"><path d="M512 352L232 672h560L512 352z" fill="#d81e06" p-id="6309"></path></svg></span>
              &nbsp;&nbsp;&nbsp;
              <span>日同比 19.16%  <svg t="1663060655984" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7210" width="16" height="16"><path d="M512 672l280-320H232l280 320z" fill="#1afa29" p-id="7211"></path></svg></span>
            </template>
            <template slot="footer">
              <span>日销售额￥ 12423</span>
            </template>
          </detail>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card>
          <!-- 第二个card -->
          <detail title="访问量" count="88460">
            <template slot="charts">
              <lineCharts></lineCharts>
            </template>
            <template slot="footer">
              <span>日访问量 1234</span>
            </template>
          </detail>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card>
          <!-- 第三个card -->
          <detail title="支付笔数" count="88460">
            <template slot="charts">
              <barCharts></barCharts>
            </template>
            <template slot="footer">
              <span>转化率 65%</span>
            </template>
          </detail>
        </el-card>
      </el-col>
      <el-col :span="6">
        <el-card>
          <!-- 第四个card -->
          <detail title="运营活动效果" count="78%">
            <template slot="charts">
              <progressCharts></progressCharts>
            </template>
            <template slot="footer">
              <span>周同比 12%  <svg t="1663060529876" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="6308" width="16" height="16"><path d="M512 352L232 672h560L512 352z" fill="#d81e06" p-id="6309"></path></svg></span>
              &nbsp;&nbsp;&nbsp;
              <span>日同比 11%  <svg t="1663060655984" class="icon" viewBox="0 0 1024 1024" version="1.1" xmlns="http://www.w3.org/2000/svg" p-id="7210" width="16" height="16"><path d="M512 672l280-320H232l280 320z" fill="#1afa29" p-id="7211"></path></svg></span>
            </template>
          </detail>
        </el-card>
      </el-col>
    </el-row>
  </div>
</template>

<script>
  import lineCharts from './lineChart'
  import Detail from './Detail'
  import barCharts from './barCharts'
  import progressCharts from './progressCharts'
export default {
  components:{
    Detail,
    lineCharts,
    barCharts,
    progressCharts
  }
}
</script>

<style>
</style>