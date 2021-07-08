<template>
  <div class="slot">
    {{ slogMsg }}
    <div class="slot_container">
      <!-- <slot name="abc">这里有个默认值</slot>
      <slot name="def"></slot> -->
      <slot txt="ceshi"></slot>
    </div>
  </div>
</template>

<script>
export default {
  name: "slot",
  data() {
    return {
      slogMsg: "这里测试slot",
    };
  },
  components: {},
};
</script>

<style scoped>
.slot_container {
  width: 100%;
  height: 100px;
  border: 1px solid gray;
  background-color: aquamarine;
}
</style>
