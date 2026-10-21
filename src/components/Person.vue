<!-- 子组件 -->
<template>
  <div class="person">
    <h3>Person 子组件</h3>
    <h3>姓名：{{ username }}</h3>
    <!-- 绑定事件语法@， v-on -->
    <button @click="showPhone">显示联系方式</button>
    <button v-on:click="showPhone">显示联系方式</button>
  </div>
</template>

<!-- 不写采用默认文件名作为组件名 -->
<!-- <script lang="ts">
  export default {
    name: "PersonVue",
  };
</script> -->
<!-- setup 语法糖，使用name需要安装插件 -->
<script lang="ts" setup name="PersonVue">
  let username = "test123123213";

  let phone = "18989899898";

  //定义函数
  function showPhone() {
    alert(phone);
  }
  // //可以返回函数
  // return {
  //   username,
  //   showPhone,
  // };
  // //渲染函数，会覆盖template
  // return function () {
  //   return "渲染函数";
  // };
</script>

<style scoped>
  .person {
    background-color: orange;
    box-shadow: 0 0 15px;
    border-radius: 15px;
    padding: 15px;
  }

  button {
    margin-left: 5px;
  }
</style>
