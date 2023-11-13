<template>
  <div>
    <h1 class="heading">Class and Style Binding</h1>
    <h1 v-bind:style="{ color: colorKey }">Style Bindings</h1>
    <h1 v-bind:class="{ display: show, displaycolor: show }">
      Class binding with objects
    </h1>
    <h1 v-bind:class="[aClass]">Class binding with array</h1>
    <h1 v-bind:class="[show ? 'yesShow' : 'noShow']">
      Class binding with array conditional case
    </h1>
  </div>
</template>
<script>
export default {
  name: "StyledComponent",
  data() {
    return {
      show: true,
      aClass: "arrayClass",
      colorKey: "brown",
    };
  },
};
</script>
<style scoped>
.heading {
  background-color: darkgrey;
  color: rgb(215, 28, 15);
}
.display {
  background-color: black;
  color: whitesmoke;
}
.arrayClass {
  background-color: cyan;
}
</style>
