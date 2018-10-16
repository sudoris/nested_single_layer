<template>  
  <div>
    

    <input type="text" v-model="value.keyOnCreate.newnew">
    <p>{{ value }} in Child</p>
    <GrandChild v-model="value.keyOnCreate"/>
    <p>{{ value }} in Child 2</p>
   
    
  </div>
</template>

<script>
import GrandChild from "./GrandChild";

export default {
  props: ["value"],
  data() {
    return {
      // value: { name: "David" }
    };
  },
  methods: {
    changeValue() {}
  },
  // watch: {
  //   value: function() {
  //     this.$emit("myEvent", this.value);
  //   }
  // },
  created() {
    this.$set(this.value, "keyOnCreate", {});
    //this.value["keyOnCreate"] = {};
    this.$emit("input", this.value);
  },
  components: {
    GrandChild
  }
};
</script>

<style>
</style>
