<script>
export default {
  data() {
    return {
      names: [
			{
				id: 1,
				value: 'name1',
			},
			{
				id: 2,
				value: 'name2',
			},
			{
				id: 3,
				value: 'name3',
			},
		]
    }
  },
  methods: {
    }
}
</script>
<template>
  <ul v-for="smh in names" :key="smh.id">
    <li>{{ smh.value }}</li>
  </ul>
</template>


<style>
  table {
    display: flex;
    justify-content: flex-start;
    flex-direction: column-reverse;
  }
</style>

<style >
.button {
    background-color: #00eeff; /* Green */
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
</style>