<template>
  <div>
    <h1>1. Home component Called</h1>
    <h2>2.Data Passing Props {{ data }} : {{ msg }}</h2>
    <button v-on:click="hello('hello called')">3. Call Hello function</button>
    <h1 v-if="show">4. vue conditional rendering if block</h1>
    <h1 v-else>4. vue conditional rendering else block</h1>
    <button v-on:click="display">Toggle 4th point Element</button>
  </div>
</template>
<script>
export default {
  name: "HomeComponent",
  props: {
    data: String,
    msg: String,
  },
  methods: {
    hello(data) {
      console.log(data);
    },
    display() {
      this.show = !this.show;
    },
  },
  data() {
    return { show: true };
  },
};
</script>
