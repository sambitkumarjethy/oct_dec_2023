<template>
  <div>
    <h1>Child component</h1>
    <b>{{ name }}-{{ userName }}</b>
    <h3 v-for="user in users" :key="user.name">
      {{ user.name }}__________{{ user.email }}
    </h3>
  </div>
</template>
<script>
export default {
  name: "ChildComponent",
  props: ["name", "userName", "users"],
};
</script>
