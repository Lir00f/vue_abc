<script>
export default {
  data() {
    return {
      customers: [
        {
          id: 1,
          name: "Alex",
          value: 100,
          age: 30,
        },
        {
          id: 2,
          name: "Diana",
          value: 200,
          age: 40,
        },
        {
          id: 3,
          name: "Polina",
          value: 300,
          age: 50,
        },
      ],
    };
  },
  methods: {
    removeItem: function (id) {
      this.customers = this.customers.filter((customer) => {
        return customer.id !== id;
      });
    },
  },
};
</script>
<template>
  <table>
    <tr>
      <th>Id</th>
      <th>Name</th>
      <th>Salary</th>
      <th>Age</th>
      <th>Remove</th>
    </tr>
    <tr v-for="customer in customers">
      <td>{{ customer.id }}</td>
      <td>{{ customer.name }}</td>
      <td>{{ customer.value }}</td>
      <td>{{ customer.age }}</td>
      <td><button class="button" @click="removeItem(customer.id)">remove</button></td>
    </tr>
  </table>
</template>

<style >
.button {
    background-color: #46ace7; /* Green */
    border-radius: 8px;
    border: none;
    color: rgb(0, 0, 0);
    padding: 15px 32px;
    text-align: center;
    text-decoration: none;
    display: inline-block;
    font-size: 16px;
    margin: 4px 2px;
    cursor: pointer;
    -webkit-transition-duration: 0.4s; /* Safari */
    transition-duration: 0.4s;
}
.active {
  border: 5px solid green;
}
.valid {
  color: blue;
}
</style>