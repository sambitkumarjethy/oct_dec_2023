<template>
  <div id="app">
    <!-- <img alt="Vue logo" src="./assets/logo.png" />
    <HelloWorld msg="Welcome to Your Vue.js App" /> -->
    <HomeComponent data="sambit" msg="Hi from sambit" />
    <HomeComposing />
    <TemplateComponet />
    <StyledComponent />
    <DataBind />
    <h1>{{ title }}</h1>
    <ChildComponent
      name="sambit Jethy"
      v-bind:userName="userName"
      v-bind:users="users"
      v-on:changeTitle="updateTitle($event)"
    />
    <SignUp />
    <LoginComponent />
    <FormValidation />
    <hr />
    <h1>Filters</h1>
    <ul>
      <li>It is global scope - once declared can be used any where</li>
    </ul>
    <h5>{{ name | Ucase }}</h5>
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
import SignUp from "./components/SignUp.vue";
import LoginComponent from "./components/LoginComponent.vue";
import FormValidation from "./components/FormValidation.vue";
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
    SignUp,
    LoginComponent,
    FormValidation,
  },
  data() {
    return {
      userName: "Babaul Jethy",
      title: "Props tutorial  child to parent App component title here",
      users: [
        { name: "Anil", email: "anil@test.com" },
        { name: "sidhu", email: "anil11@test.com" },
        { name: "sam", email: "anil2@test.com" },
        { name: "Kesab", email: "anilrr@test.com" },
        { name: "maharaj", email: "anilgg@test.com" },
        { name: "Swami", email: "anilcc@test.com" },
      ],
      name: `Sambit - here is the example of filters using "Ucase" defined filter in main.js`,
    };
  },
  methods: {
    updateTitle(title) {
      this.title = title;
    },
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
