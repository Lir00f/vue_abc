<script>
import Employee from './components/Employee.vue'
export default {
  data() {
    return {
      developers: [
        {
          id: 1,
          name: 'Milana',
          surn: 'Prikolovna'
        },
        {
          id: 2,
          name: 'Polina',
          surn: 'Bebrusovna'
        },
        {
          id: 3,
          name: 'Emran',
          surn: 'Jujubiev'
        },
      ],
    }
  },
  components: {
    Employee
  },
  methods: {
    change(id, name, surn){
      this.developers = this.developers.map((developer) => {
        if(developer.id === id){
          developer.name = name;
          developer.surn = surn;
        }
        return developer;
      });
    }
  }
}
</script>

<template>
<Employee v-for   ="developer in developers"
		:id     ="developer.id"
		:name   ="developer.name"
		:surn   ="developer.surn"
		:key    ="developer.id"
    @change="change"/>
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