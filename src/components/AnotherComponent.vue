<template>
  <div class="template">
    <hr />
    <!-- <h1>Template in Vue JS</h1> -->
    {{rawHtml}}
    <p v-html="rawHtml" />
    <h2 v-once>{{name}}</h2>
    <h2>{{name}}</h2>
    <h2>{{10+19}}</h2>
    <h2>{{a+b}}</h2>
    <button v-on:click="updateText">Click Me</button>
    <button v-bind:disabled="disablebtn" v-on:click="updateText">Click Me</button>

    <h3>{{ok?"YES":"NO"}}</h3>
  </div>
</template>

<script>
export default {
  name: "AnotherComponent",
  data() {
    return {
      name: "Shubham",
      a: 10,
      b: 20,
      ok: true,
      rawHtml: "<h1>Template in Vue JS</h1>",
      disablebtn: true
    };
  },
  methods: {
    updateText() {
      this.name = "Peter";
      this.ok = !this.ok;
    }
  }
};
</script>

<style>
</style>