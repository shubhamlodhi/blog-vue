<template>
  <div>
    <h1>Hello From Home Component</h1>
    <h2>{{data}}</h2>
    <h3>{{msg}}</h3>
  </div>
</template>

<script>
export default {
  name: "Home",
  props: {
    data: String,
    msg: String
  }
};
</script>

<style>
</style>