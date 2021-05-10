<template>
  <div class="maincontent">
    <div class="todo1">
      右上角登陆，点击进登陆页
    </div>
    <div class="todo">
      提醒通知（带定时功能）
      个人网站收藏
      日历
      记事本（gitbook）
      代码部署
      cli工具
      工作台
      图表
      记账系统带导表功能
      个人喜欢的咨询定制
      图标库
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
    return { count }
  }
})
</script>
<style scoped lang="less">

</style>
