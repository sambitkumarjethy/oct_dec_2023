<template>
  <div>
    <h1>Home - Composing component</h1>
    <b>Call of user component using import</b>
    <UsersComponent />
    <ProductComponent />
  </div>
</template>
<script>
import ProductComponent from "./ProductComponent.vue";
import UsersComponent from "./UsersComponent.vue";
export default {
  name: "HomeComposing",
  components: {
    UsersComponent,
    ProductComponent,
  },
};
</script>
<style scoped>
div {
  background-color: #b4b4b4;
  height: 500px;
}
</style>
