<!-- 编写模版 -->
<template>
  <!-- 编写html -->
  <div class="hello">
    <h1>hello vue3</h1>
    <!-- 使用组件 -->
    <Person></Person>
  </div>
</template>
<!-- 编写ts脚本 -->
<script lang="ts">
  //导入person组件
  import Person from "./components/Person.vue";

  //默认导出
  export default {
    name: "app",
    //组件注册
    components: { Person },
  };
</script>
<!-- 编写样式 -->
<style scoped>
  .hello {
    background-color: red;
    box-shadow: 0 0 15px;
    border-radius: 15px;
    padding: 15px;
  }
</style>
