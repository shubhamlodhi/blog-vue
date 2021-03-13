<template>
  <div class="parent">
    <h1>This is ParentComponent</h1>
    <ChildComponent />
    <ChildComponent2 />
  </div>
</template>

<script>
import ChildComponent from "./ChildComponent.vue";
import ChildComponent2 from "./ChildComponent2.vue";

export default {
  name: "ParentComponent",

  components: {
    ChildComponent,
    ChildComponent2
  }
};
</script>

<style>
.parent {
  background-color: grey;
  padding: 15px;
}
</style>