<script>
export default {
  data() {
    return {
      visibility: false,
    }
  },
  methods: {
    changeVisibility: function() {
      this.visibility = !this.visibility
    }
  }
}
</script>
<template>
  <p v-if="!visibility">P1</p>
  <p v-else>P2</p>
  <button class="button" @click="changeVisibility">visibility = {{ visibility }}</button>
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