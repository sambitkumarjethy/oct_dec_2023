<template>
  <div>
    <hr />
    <h1>SignUp Form</h1>
    <input
      type="text"
      placeholder="Enter yout name"
      v-model="signup.username"
    />
    <br /><br />
    <input
      type="password"
      placeholder="Enter your password"
      v-model="signup.password"
    />
    <br /><br />
    <p>Choose Hobbies</p>
    <input
      type="checkbox"
      id="cricket"
      value="cricket"
      v-model="signup.hobbies"
    />
    <label for="cricket"> Cricket </label>
    <input
      type="checkbox"
      id="football"
      value="football"
      v-model="signup.hobbies"
    />
    <label for="football"> Foot Ball </label>
    <br /><br />
    <p>Select Gender</p>
    <input
      type="radio"
      id="male"
      name="gender"
      value="male"
      v-model="signup.gender"
    />
    <label for="male"> Male </label>
    <input
      type="radio"
      id="female"
      name="gender"
      value="female"
      v-model="signup.gender"
    />
    <label for="female"> Female </label>
    <br />
    <button v-on:click="signupUser">Sign Up</button>
  </div>
</template>
<script>
export default {
  name: "SignUp",
  data() {
    return {
      signup: {
        username: null,
        password: null,
        hobbies: [],
        gender: null,
      },
    };
  },
  methods: {
    signupUser() {
      console.warn(this.signup);
    },
  },
};
</script>
