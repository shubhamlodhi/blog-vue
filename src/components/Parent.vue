<template>
  <h1>{{title}}</h1>
  <Child
    v-on:changeTitle="updateTitle($event)"
    name="Shubham"
    v-bind:surname="surName"
    v-bind:users="users"
  />
</template>

<script>
import Child from "./Child.vue";
export default {
  name: "Parent",
  components: { Child },
  data() {
    return {
      surName: "lodhi",
      users: [{ name: "a" }, { name: "b" }, { name: "c" }],
      title: "This is Parent"
    };
  },

  methods: {
    updateTitle(title) {
      this.title = title;
    }
  }
};
</script>

<style>
</style>