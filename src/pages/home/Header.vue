<template>
  <div class="travel_header">
    <p @click="changePropsData">这里是top组件---{{ acceptData }}</p>
  </div>
</template>

<script>
import { mixinsFunction } from "../../mixin.js";
export default {
  name: "travel_header",
  mixins: [mixinsFunction],
  props: ["dataSend"],
  data() {
    return {
      msg: "这里是头部",
      //   acceptData: JSON.parse(JSON.stringify(this.dataSend)),
      acceptData: this.deepClone1(this.dataSend),
    };
  },
  computed: {
    // acceptData: function () {
    //   return this.dataSend;
    // },
  },
  methods: {
    changePropsData() {
      this.acceptData.b = 3;
    },
    deepClone1(obj) {
      //判断拷贝的要进行深拷贝的是数组还是对象，是数组的话进行数组拷贝，对象的话进行对象拷贝
      var objClone = Array.isArray(obj) ? [] : {};
      //进行深拷贝的不能为空，并且是对象或者是
      if (obj && typeof obj === "object") {
        for (var key in obj) {
          if (obj.hasOwnProperty(key)) {
            if (obj[key] && typeof obj[key] === "object") {
              objClone[key] = deepClone1(obj[key]);
            } else {
              objClone[key] = obj[key];
            }
          }
        }
      }
      return objClone;
    },
  },
  //   mounted() {
  //     this.changePropsData();
  //   },
};
</script>

<style scoped>
</style>
