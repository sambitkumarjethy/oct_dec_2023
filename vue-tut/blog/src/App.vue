<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <HomeComponent data="sambit" msg="Hi from sambit" />
    <HomeComposing />
    <TemplateComponet />
    <StyledComponent />
    <DataBind />
    <ChildComponent
      name="sambit Jethy"
      v-bind:userName="userName"
      v-bind:users="users"
    />
    <!-- <HomeComponent data="Jethy" /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import HomeComponent from "./components/HomeComponent.vue";
import HomeComposing from "./components/HomeComposing.vue";
import TemplateComponet from "./components/TemplateComponent.vue";
import StyledComponent from "./components/StylledComponent.vue";
import DataBind from "./components/DataBind.vue";
import ChildComponent from "./components/ChildComponent.vue";
export default {
  name: "App",
  components: {
    // HelloWorld,
    HomeComponent,
    HomeComposing,
    TemplateComponet,
    StyledComponent,
    DataBind,
    ChildComponent,
  },
  data() {
    return {
      userName: "Babaul Jethy",
      users: [
        { name: "Anil", email: "anil@test.com" },
        { name: "sidhu", email: "anil11@test.com" },
        { name: "sam", email: "anil2@test.com" },
        { name: "Kesab", email: "anilrr@test.com" },
        { name: "maharaj", email: "anilgg@test.com" },
        { name: "Swami", email: "anilcc@test.com" },
      ],
    };
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
