<script>
export default {
  data() {
    return {
      visibility: true,
    }
  },
  methods: {
    toggle: function() {
      this.visibility = !this.visibility;
    }
  }
}
</script>
<template>
  <div v-if="visibility">
  <p>1</p>
  <p>2</p>
  <p>3</p>
  </div>
  <button class="button" @click="toggle">тык</button>
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