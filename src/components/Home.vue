<template>
  <div>
    <h1>Hello From Home Component</h1>
    <h2>{{data}}</h2>
    <h3>{{msg}}</h3>

    <!-- Events -->
    <button v-on:click="hello">Call Hello Function</button>
    <button v-on:click="hello2('Hello from hello2 function')">Call Hello2 Function</button>
    <button v-on:mouseover="hello2('Hello from hello2 function')">Call Hello2 Function</button>

    <!-- Conditional Rendering -->
    <h1 v-if="show">If Block : Conditional Rendering in Vue</h1>
    <h1 v-else>Else Block : Conditional Rendering from else block in Vue</h1>
    <button v-on:click="display">Toggle Element</button>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    data: String,
    msg: String
  },
  methods: {
    hello() {
      console.log("Hello Function Called Console");
    },

    hello2(data) {
      alert(data);
    },

    display() {
      this.show = !this.show;
    }
  },
  data() {
    return { show: false };
  }
};
</script>

<style>
</style>