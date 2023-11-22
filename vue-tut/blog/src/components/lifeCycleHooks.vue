<template>
  <div>
    <hr />
    <h1>Life Cycle methods</h1>
    <h3>Create Mehthod - {{ name }}</h3>
    <h3 v-if="display">{{ subject }}</h3>
    <button v-on:click="toggle">Toggle</button>
  </div>
</template>
<script>
export default {
  name: "LifeCycleMethod",
  data() {
    return {
      name: "This is life cycle hooks tutorial.",
      subject: "Vuejs",
      display: true,
    };
  },
  methods: {
    toggle() {
      this.display = !this.display;
    },
  },
  beforeDestroy() {
    console.warn("before destroy");
  },
  destroted() {
    console.warn("destroted");
  },
  created() {
    this.name = "* data updated while  create method.";
    console.warn("created from life cycle hook", this.name);
  },
  beforeCreate() {
    this.name = "before craete name";
    console.warn("before from life cycle hook", this.name);
  },
  beforeMount() {
    console.warn("beforeMount", this.$el);
  },
  mounted() {
    console.warn("mounted", this.$el); // $el is the html component
  },
};
</script>
