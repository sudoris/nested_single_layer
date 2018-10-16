<template>  
  <div>
    <input type="text" v-model="value.nk">
    <p>{{ value }} in GrandChild</p>
  </div>
</template>

<script>
export default {
  props: ["value"],
  data() {
    return {
      // value: { name: "David" }
    };
  },
  methods: {
    addKey() {}
  }
  // watch: {
  //   value: function() {
  //     this.$emit("myEvent", this.value);
  //   }
  // }
};
</script>

<style>
</style>
