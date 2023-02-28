<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      
    }
  },
  components: {
    Employee
  },
  methods: {
    prikolovni() {
      alert('Dasha, Polina, Milana');
    },
    bebrusovi(){
      alert('Lucy, Ilyuha, Leha')
    }
  }
}
</script>

<template>
<Employee @show="prikolovni" @show1="bebrusovi" />
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