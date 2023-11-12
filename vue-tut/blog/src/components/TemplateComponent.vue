<template>
  <div>
    <h1>Template in Vue js</h1>
    <h3 v-once>
      Define Constant using
      <span style="color: red">v-once</span>
      {{ name }}
    </h3>
    <h3>{{ name }}</h3>
    <h3>Button Clicked - {{ success ? "Yes" : "No" }}</h3>
    <h3>Adding variables ________ {{ 10 + 19 }}-------{{ a + b }}</h3>

    <button v-on:click="updateText">Click me</button>
    <br />
    <button v-bind:disabled="disableBtn" v-on:click="disableBtnFn">
      Disable btn using <span style="color: red">v-bind</span>
    </button>
    <p v-html="rowHtml" />
  </div>
</template>
<script>
export default {
  name: "TemplateComponet",
  data() {
    return {
      name: "Sambit jethy",
      a: 10,
      b: 20,
      success: false,
      rowHtml:
        "<h1>print Html Tag using <span style='color: red'>v-html </span></h1>",
      disableBtn: true,
    };
  },
  methods: {
    updateText() {
      this.name = "jethy Sambit";
      this.success = true;
      this.disableBtn = false;
    },
    disableBtnFn() {
      this.disableBtn = true;
      this.success = !this.success;
      this.name = "Sambit jethy";
    },
  },
};
</script>
