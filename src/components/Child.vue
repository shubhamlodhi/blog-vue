<template>
  <h1>This is Child</h1>
  <h2>{{name}}</h2>
  <h3>{{surname}}</h3>
  <h4 v-for="user in users" :key="user.name">{{user.name}}</h4>
  <h1>Send prop to Parent to update parent title</h1>
  <button v-on:click="updateTitle($event)">Update Parent Title</button>
</template>

<script>
export default {
  name: "Child",
  props: ["name", "surname", "users"],
  methods: {
    updateTitle() {
      this.$emit("changeTitle", "Parent Updated");
    }
  }
};
</script>

<style>
</style>