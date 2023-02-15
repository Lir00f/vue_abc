<script>
export default {
  data() {
    return {
      values: [1, 3, 5, -4, 7],
    }
  },
  methods: {
    }
}
</script>
<template>
  <div v-for="value in values">
    <p v-if="value >= 0">{{ value }}&nbsp;</p>
  </div>
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