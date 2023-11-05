<template>
  <div>
    <h1>Hello from Home component</h1>
    <h2>{{ data }} : {{ msg }}</h2>
    <button v-on:click="hello('hello called')">Call Hello function</button>
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
  },
};
</script>
