<script>
export default {
  data() {
    return {
      items: [321,423,53,42,57],
    }
  },
  methods: {
    }
}
</script>
<template>
    <div class="red-box"><div v-for="elem in items">{{ elem }} &nbsp;</div></div> <br>
    <div class="red-box"><br><div v-for="elem in items">{{ elem ** 2 }} &nbsp;</div></div> <br> <br>
    <div class="red-box right"><div v-for="elem in items"><ul><li>{{ elem }}</li></ul>&nbsp;</div></div>
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