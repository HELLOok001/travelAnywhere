<template>
  <div class="hello">
    <travelHeader></travelHeader>
    {{ msg }}
  </div>
</template>

<script>
import travelHeader from "./Header";
export default {
  name: "Home",
  data() {
    return {
      msg: "这里要开始测试项目了",
    };
  },
  components: {
    travelHeader,
  },
};
</script>

<style scoped>
</style>
