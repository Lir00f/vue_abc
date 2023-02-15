<script>
export default {
  data() {
    return {
      arr: ['a', 'b', 'c'],
    }
  },
  methods: {
    }
}
</script>
<template>
  <p class ="button" v-for="(elem, klych) in arr">{{ klych }}:&nbsp {{ elem }}</p>
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