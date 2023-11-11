<template>
  <div>
    <h1>1. Home component Called</h1>
    <h2>2.Data Passing Props {{ data }} : {{ msg }}</h2>
    <button v-on:click="hello('hello called')">3. Call Hello function</button>
    <h1 v-if="show">4. vue conditional rendering if block</h1>
    <h1 v-else>4. vue conditional rendering else block</h1>
    <button v-on:click="display">Toggle 4th point Element</button>
    <h1>5. For loop in vue js</h1>
    <table border="1px">
      <tr>
        <td>Id</td>
        <td>Name</td>
        <td>Email</td>
      </tr>
      <tr v-for="user in users" :key="user.id">
        <td>{{ user.id }}</td>
        <td>{{ user.name }}</td>
        <td>{{ user.email }}</td>
      </tr>
    </table>
  </div>
</template>
<script>
export default {
  name: "HomeComponent",
  props: {
    data: String,
    msg: String,
  },
  methods: {
    hello(data) {
      console.log(data);
    },
    display() {
      this.show = !this.show;
    },
  },
  data() {
    return {
      show: true,
      users: [
        { id: 1, name: "Sambit", email: "s@g.com" },
        { id: 2, name: "Petter", email: "p@g.com" },
        { id: 3, name: "watson", email: "w@g.com" },
        { id: 4, name: "Dhoni", email: "d@g.com" },
        { id: 5, name: "kuldeep", email: "k@g.com" },
      ],
    };
  },
};
</script>
