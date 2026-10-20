<!-- 子组件 -->
<template>
  <div class="person">
    <h3>姓名：{{ username }}</h3>
    <!-- 绑定事件语法@， v-on -->
    <button @click="showPhone">显示联系方式</button>
    <button v-on:click="showPhone">显示联系方式</button>
  </div>
</template>

<script lang="ts">
  export default {
    name: "PersonVue",
    setup() {
      let username = "test123123213";

      let phone = "18989899898";

      //定义函数
      function showPhone() {
        alert(phone);
      }

      return {
        username,
        showPhone,
      };
    },
  };
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
