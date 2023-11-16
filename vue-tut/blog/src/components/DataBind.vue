<template>
  <div>
    <h1>BIND DATA IN Vue JS</h1>
    <h5 style="white-space: pre-line">{{ message }}</h5>
    <input type="text" v-model="message" />
    <br />
    <textarea type="text" v-model="message" />
  </div>
</template>
<script>
export default {
  name: "DataBind",
  data() {
    return {
      message: "Hi sambit",
    };
  },
};
</script>
