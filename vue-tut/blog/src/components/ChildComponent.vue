<template>
  <div>
    <hr />
    <h1>Child component</h1>
    <b>{{ name }}-{{ userName }}</b>
    <h3 v-for="user in users" :key="user.name">
      {{ user.name }}__________{{ user.email }}
    </h3>
    <hr />
    <h1>Send Data from child to parrent</h1>
    <p>functions is always defined inside methods</p>
    <button v-on:click="updateTitle">Update parrent Title</button>
  </div>
</template>
<script>
export default {
  name: "ChildComponent",
  props: ["name", "userName", "users"],
  methods: {
    updateTitle() {
      this.$emit("changeTitle", "Parent Updated");
    },
  },
  beforeCreate: function () {
    console.warn("Before create");
  },
  beforeMount: function () {
    console.warn("Before mount");
  },
  mounted: function () {
    console.warn("mounted");
  },
  created: function () {
    console.warn("created");
  },
};
</script>
