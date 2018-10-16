<template>
  <div>
    <Child v-model="model" />
    <p>{{ model }} in Parent</p>
  </div>
</template>

<script>
import Child from "./Child"

export default {
  name: "HelloEvents",
  data() {
    return {
      // model: { name: "David" }
      model: { }
    };
  },
  components: {
    Child
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style>
</style>
 