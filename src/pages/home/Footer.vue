<template>
  <div class="travel_header">
    <p>{{ msg }}</p>
  </div>
</template>

<script>
export default {
  name: "travel_footer",

  data() {
    return {
      msg: "这里是底部",
    };
  },
  computed: {
    // acceptData: function () {
    //   return this.dataSend;
    // },
  },
  methods: {},
};
</script>

<style scoped>
</style>
