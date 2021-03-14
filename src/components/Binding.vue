<template>
  <h1>Class and Style Binding</h1>
  <h1 v-bind:style="{color:'blue'}">Style Binding</h1>
  <h1 v-bind:class="{display:show}">Class Binding</h1>
  <h1 v-bind:class="[aclass]">Class Bind with array</h1>
  <h1 v-bind:class="[show ?'yesShow':'noShow']">Class Bind with array</h1>
  <h2 v-bind:style="{color:colorKey}">Style by property</h2>
</template>

<script>
export default {
  name: "Binding",
  data() {
    return {
      show: true,
      aclass: "arrayClass",
      colorKey: "blue"
    };
  }
};
</script>

<style>
.display {
  background-color: brown;
}

.arrayClass {
  background-color: cyan;
}

.yesShow {
  background-color: green;
}

.noShow {
  background-color: red;
}
</style>