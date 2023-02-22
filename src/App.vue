<script>
export default {
  data() {
    return {
      obj: {
        done: true,
        selected: false,
      },
    };
  },
  methods: {},
};
</script>
<template>
  <p :class="obj">text</p>
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
.done {
  border: 5px solid blue
}
.selected {
  color: rgb(128, 0, 128);
  font-size: 12em;
}
</style>