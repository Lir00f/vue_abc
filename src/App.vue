<script>
export default {
  data() {
    return {
      visibility: false,
    }
  },
  methods: {
    changeVisibilityToTrue: function() {
      this.visibility = true;
    },
    changeVisibilityToFalse: function() {
      this.visibility = false;
    }
  }
}
</script>
<template>
  <button class="button" v-if="!visibility" @click="changeVisibilityToTrue">Show text</button>
  <button class="button" v-else @click="changeVisibilityToFalse">Hide text</button><br>
  <p v-if="visibility">text</p>
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