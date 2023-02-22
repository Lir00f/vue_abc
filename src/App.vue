<script>
export default {
  data() {
    return {
      var_1: "Task 1",
      isCtrlPressed: false,
      var_2: "ctrl+link pressed",
    };
  },
  methods: {
    lag: function () {
      this.var_1 = this.$refs.textField.value;
    },
    leg: function (event) {
      if (event.ctrlKey) {
        this.isCtrlPressed = true;
      }
    },
    handleLeftClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "left";
      }
    },
    handleRightClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "right";
      }
    },
    handleMiddleClick: function (event) {
      if (!event.ctrlKey) {
        this.var_2 = "middle";
      }
    },
  },
};
</script>
<template>
  <input type="text" @keyup.enter="lag" ref="textField" />
  &nbsp;
  <p>{{ var_1 }}</p>
  &nbsp;
  <a
    href="vk.com/id1"
    @click="leg"
    @click.left="handleLeftClick"
    @click.right="handleRightClick"
    @click.middle="handleMiddleClick"
    target="_blank"
    >Задание 2 и 3</a
  >
  &nbsp;
  <p v-if="isCtrlPressed">{{ var_2 }}</p>
</template>

<style >
.button {
    background-color: #46ace7; /* Green */
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