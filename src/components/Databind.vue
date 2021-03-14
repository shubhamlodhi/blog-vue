<template>
  <div>
    <h1>{{message}}</h1>
    <input type="text" v-model="message" />

    <h1 style="white-space:pre-line">{{message}}</h1>
    <textarea type="text" v-model="message" />
  </div>
</template>

<script>
export default {
  name: "Databind",
  data() {
    return {
      message: "Hi"
    };
  }
};
</script>

<style>
</style>