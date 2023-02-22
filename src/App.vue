<script>
export default {
  data() {
    return {
      isValid: true,
      isDisabled: true,
    };
  },
  methods: {
    setDone: function () {
      this.obj.hidden = !this.obj.hidden;
    },
  },
};
</script>
<template>

<p :class="{ active: isValid, valid: isDisabled }">Task #1</p>
</template>

<style >
.button {
    background-color: #46dde7; /* Green */
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
.active {
  border: 5px solid green;
}
.valid {
  color: blue;
}
</style>