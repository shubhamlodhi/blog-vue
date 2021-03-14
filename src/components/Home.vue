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

    <!-- For Loop -->
    <table border="1px">
      <tr>
        <td>ID:</td>
        <td>Name:</td>
        <td>Email:</td>
      </tr>

      <tr v-for="items in users" :key="items.id">
        <td>{{items.id}}</td>
        <td>{{items.name}}</td>
        <td>{{items.email}}</td>
      </tr>
    </table>

    <!-- Composition -->
    <ParentComponent />

    <AnotherComponent />

    <Binding />

    <Databind />

    <Parent />
  </div>
</template>

<script>
import ParentComponent from "./ParentComponent.vue";
import AnotherComponent from "./AnotherComponent.vue";
import Binding from "./Binding.vue";
import Databind from "./Databind.vue";
import Parent from "./Parent.vue";

export default {
  name: "Home",
  components: {
    ParentComponent,
    AnotherComponent,
    Binding,
    Databind,
    Parent
  },
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
    return {
      show: false,
      users: [
        { id: 1, name: "peter1", email: "peter1@example.com" },
        { id: 2, name: "peter2", email: "peter2@example.com" },
        { id: 3, name: "peter3", email: "peter3@example.com" },
        { id: 4, name: "peter4", email: "peter4@example.com" },
        { id: 5, name: "peter5", email: "peter5@example.com" }
      ]
    };
  }
};
</script>

<style>
</style>