<template>
  <div class="maincontent">
    <div class="todo">
      <div class="todo1">
        <h1>1.提醒通知（带定时功能）</h1>
        <h1>2.个人网站收藏</h1>
        <h1>3.日历</h1>
        <h1>4.记事本（gitbook）</h1>
        <h1>5.代码部署</h1>
        <h1>6.cli工具</h1>
        <h1>7.工作台</h1>
        <h1>8.图表</h1>
        <h1>9.记账系统带导表功能</h1>
        <h1>10.个人喜欢的咨询定制</h1>
        <h1>11.图标库</h1>
      </div>
      <div class="todo2">
        <h1>1.右上角登陆，点击进登陆页，制造一套权限系统</h1>
        <h1>2.首页主要实现导航功能</h1>
        <h1>3.数说天下，实现几个静态数据写死的图表（表格导入数据，实时渲染）</h1>
        <h1>4.</h1>
        <h1>5.</h1>
        <h1>6.</h1>
        <h1>7.</h1>
        <h1>8.</h1>
        <h1>9.</h1>
        <h1>10.</h1>
        <h1>11.</h1>
      </div>
    </div>
    
    <div class="calendar">
      <el-calendar v-model="value">
        <template #dateCell="{data}">
          <p :class="data.isSelected ? 'is-selected' : ''">
            {{ data.day.split('-').slice(1).join('-') }} {{ data.isSelected ? '✔️' : '' }}
          </p>
        </template>
      </el-calendar>
    </div>
  </div>
</template>

<script lang="ts">
//import "./test.css";
import { ref, defineComponent } from 'vue'
export default defineComponent({
  name: 'Home',
  setup: () => {
    const count = ref(0)
    const value = ref(new Date())
    return { count, value }
  }
})
</script>
<style scoped lang="less">
.defFlex(@row, @just, @align) {
  display: flex;
  flex-flow: @row nowrap;
  justify-content: @just;
  align-items: @align;
}
.maincontent {
  font-size: 18px;
  text-align: left;
  margin: 0 30px;
  .todo {
    .defFlex(row, flex-start, flex-start);
    .todo1 {
      margin-right: 100px;
      font-size: 12px;
    }
    .todo2 {
      font-size: 12px;
    }
  }
}
</style>
