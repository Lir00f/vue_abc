<script>
export default {
  data() {
    return {
      visibility_p1: false,
      visibility_p2: false,
      visibility_p3: false,
    }
  },
  methods: {
      toggle_p1: function() {
        this.visibility_p1 = !this.visibility_p1;
      },
      toggle_p2: function() {
        this.visibility_p2 = !this.visibility_p2;
      },
      toggle_p3: function() {
        this.visibility_p3 = !this.visibility_p3;
      },
  }
}
</script>
<template>
  <button class="button" @click="toggle_p1">toggle</button><br>
  <p v-if="visibility_p1">text p1</p>
  <button class="button" @click="toggle_p2">toggle</button><br>
  <p v-if="visibility_p2">text p2</p>
  <button class="button" @click="toggle_p3">toggle</button><br>
  <p v-if="visibility_p3">text p3</p>
  
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