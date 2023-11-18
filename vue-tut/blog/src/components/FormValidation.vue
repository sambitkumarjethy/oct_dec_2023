<template>
  <div>
    <hr />
    <h1>Form Validation</h1>
    <div v-if="error.length">
      <h3>Please currect the follwing errord</h3>
      <ul>
        <li v-for="e in error" v-bind:key="e.id">
          {{ e }}
        </li>
      </ul>
    </div>
    <form @submit="login">
      <input type="text" placeholder="enter name" v-model="name" />
      <br /><br />
      <input type="password" placeholder="enter password" v-model="password" />
      <br /><br />
      <button type="submit">Login</button>
    </form>
  </div>
</template>
<script>
export default {
  name: "FormValidation",
  data() {
    return {
      error: [],
      name: null,
      password: null,
    };
  },
  methods: {
    login(e) {
      this.error = [];
      if (this.name && this.error) {
        console.warn("No error");
      }
      if (!this.name) {
        this.error.push("User name is required");
      }
      if (!this.password) {
        this.error.push("Password is required");
      }
      e.preventDefault();
      console.warn("H@llo", this.error);
    },
  },
};
</script>
