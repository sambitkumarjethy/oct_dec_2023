<template>
  <div>
    <hr />
    <h1>Login Component</h1>
    <input
      type="text"
      name="username"
      placeholder="enter user name"
      v-model="loginForm.username"
    />
    <br /><br />
    <input
      type="password"
      name="password"
      placeholder="enter password"
      v-model="loginForm.password"
    />
    <br /><br />
    <button v-on:click="loginData">Login</button>
  </div>
</template>
<script>
export default {
  name: "LoginComponent",
  methods: {
    loginData() {
      console.log(
        "Login submited",
        this.loginForm.username,
        this.loginForm.password
      );
    },
  },
  data() {
    return { loginForm: { username: null, password: null } };
  },
};
</script>
