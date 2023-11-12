<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <HomeComponent data="sambit" msg="Hi from sambit" />
    <HomeComposing />
    <TemplateComponet />
    <!-- <HomeComponent data="Jethy" /> -->
  </div>
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
import HomeComponent from "./components/HomeComponent.vue";
import HomeComposing from "./components/HomeComposing.vue";
import TemplateComponet from "./components/TemplateComponent.vue";
export default {
  name: "App",
  components: {
    // HelloWorld,
    HomeComponent,
    HomeComposing,
    TemplateComponet,
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
