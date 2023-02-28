<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: 'Milana',
          salary: 19000,
          age: 19
        },
        {
          id: 2,
          name: 'Dasha',
          salary: 1000,
          age: 18
        },
        {
          id: 3,
          name: 'Polina',
          salary: 3000,
          age: 25
        },
      ],
    }
  },
  components: {
    Employee
  }
}
</script>

<template>
<Employee v-for="developer in developers" :name="developer.name" :salary="developer.salary" :age="developer.age" :key="developer.id" />
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