<template>
  <div>
    <hr />
    <h1>Life Cycle methods</h1>
    <h3>{{ name }}</h3>
  </div>
</template>
<script>
export default {
  name: "LifeCycleHook",
  data() {
    return {
      name: "This is life cycle hooks tutorial.",
    };
  },
  created() {
    this.name = "* data updated while  create method.";
    console.warn("created from life cycle hook", this.name);
  },
  beforeCreate() {
    this.name = "before craete name";
    console.warn("before from life cycle hook", this.name);
  },
};
</script>
