<template>
  <div>
    <hr />
    <h1>Emplyee list - Axios API call</h1>
    <div>
      <table border="1">
        <tr>
          <th>firstName</th>
          <th>lastName</th>
          <th>gender</th>
        </tr>
        <tr v-for="item in list" v-bind:key="item.id">
          <td>{{ item.firstName }}</td>
          <td>{{ item.lastName }}</td>
          <td>{{ item.gender }}</td>
        </tr>
      </table>
    </div>
  </div>
</template>
<script>
import Vue from "vue";
import VueAxios from "vue-axios";
import axios from "axios";
Vue.use(VueAxios, axios);
export default {
  name: "EmployeeList",
  data() {
    return {
      list: undefined,
    };
  },
  mounted() {
    Vue.axios.get(`https://dummyjson.com/users`).then((resp) => {
      this.list = resp.data.users;
    });
  },
};
</script>
