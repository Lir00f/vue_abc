<script>
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: "Alex",
          salary: 100,
          age: 30,
          isEdit: false,
        },
        {
          id: 2,
          name: "Diana",
          salary: 200,
          age: 40,
          isEdit: false,
        },
        {
          id: 3,
          name: "Polina",
          salary: 300,
          age: 50,
          isEdit: false,
        },
      ],
    };
  },
  methods: {
    removeItem: function (id) {
      this.developers = this.developers.filter((developer) => {
        return developer.id !== id;
      });
    },
    edit: function (developer) {
      developer.isEdit = true;
    },
    save: function (developer) {
      developer.isEdit = false;
    },
  },
};
</script>
<template>
  <table>
    <tr>
      <th>ID</th>
      <th>Имя</th>
      <th>Зарплата</th>
      <th>Возраст</th>
    </tr>
    <tr v-for="developer in developers">
      <template v-if="!developer.isEdit">
        <td>{{ developer.id }}</td>
        <td>{{ developer.name }}</td>
        <td>{{ developer.salary }}</td>
        <td>{{ developer.age }}</td>
        <td><button @click="removeItem(developer.id)">remove</button></td>
        <td><button @click="edit(developer)">edit</button></td>
      </template>
      <template v-else>
        <td><input v-model="developer.id" /></td>
        <td><input v-model="developer.name" /></td>
        <td><input v-model="developer.salary" /></td>
        <td><input v-model="developer.age" /></td>
        <td><button @click="save(developer)">save</button></td>
      </template>
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