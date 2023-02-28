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
          surn: 'Bebrusova'
        },
        {
          id: 3,
          name: 'Jujuba',
          surn: 'Fandeev'
        },
      ],
    }
  },
  components: {
    Employee
  },
  methods: {
    remove(id) {
      this.developers = this.developers.filter((developer) => {
        return developer.id !== id;
      })
    }
  }
}
</script>

<template>
<Employee v-for   ="developer in developers"
		:id     ="developer.id"
		:name   ="developer.name"
		:surn   ="developer.surn"
		@remove ="remove"
		:key    ="developer.id"/>
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