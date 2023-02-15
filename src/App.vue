<script>
export default {
  data() {
    return {
      data: {
      user1: '1000',
      user2: '2000',
      user3: '5000',
      }
    }
  },
  methods: {
    }
}
</script>
<template>
  <ul>
    <li v-for="value in data">{{ value }}</li>
  </ul>
  <ul>
    <li v-for="(value, key) in data">{{ key }} - {{ value }}</li>
  </ul>
  <ul>
    <li v-for="(value, key, index) in data">{{ key }} - {{ value }} - {{ index }}</li>
  </ul>
  <ul>
    <li v-for="(value, key, index) in data">{{ key }} - {{ value }} - {{ index + 1 }}</li>
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