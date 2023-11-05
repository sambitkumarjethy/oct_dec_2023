<template>
  <div>
    <h1>Hello from Home component</h1>
    <h2>{{ data }} : {{ msg }}</h2>
  </div>
</template>
<script>
export default {
  name: "HomeComponent",
  props: {
    data: String,
    msg: String,
  },
};
</script>
