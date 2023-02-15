<script>
export default {
  data() {
    return {
      value: [1000, 2000, 5000],
    }
  },
  methods: {
    }
}
</script>
<template>
  	<template v-for="obj in value">
		<p>&nbsp;{{ obj }}&nbsp;</p>
		<hr>
    </template>
    <ul v-for="obj in value">
      <li>
        <p>&nbsp;{{ obj }}&nbsp;</p>
      </li>
      <hr>
    </ul>
</template>

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