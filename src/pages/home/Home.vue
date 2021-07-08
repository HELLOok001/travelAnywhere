<template>
  <div class="hello">
    <travelHeader :dataSend="obj"></travelHeader>
    <travelHeader :dataSend="obj"></travelHeader>
    <slotTest>
      <!-- <div style="background-color: skyblue; color: #ccc" slot="abc">
        1111111111111111
      </div>
      <div style="background-color: brown; color: #ccc" slot="def">222222</div> -->
      <template slot-scope="props">
        <div>{{ props.txt }}</div>
      </template>
    </slotTest>
    <component :is="component_name"></component>
    {{ msg }}
  </div>
</template>

<script>
import travelHeader from "./Header";
import travelFooter from "./Footer";
import slotTest from "./slot_test.vue";
export default {
  name: "Home",
  data() {
    return {
      msg: "这里要开始测试项目了",
      obj: {
        a: 1,
        b: 2,
      },
      component_name: "travelFooter",
    };
  },
  components: {
    travelHeader,
    slotTest,
    travelFooter,
  },
};
</script>

<style scoped>
</style>
