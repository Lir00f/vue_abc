<script>
export default {
  data() {
    return {
      obj: {
        hidden: true,
      },
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
  <button class="button" @click="this.obj.hidden = false">hide Задание 2</button>
  <button class="button" @click="this.obj.hidden = true">hide Задание 3</button>
  <button class="button" @click="setDone">{{ obj.hidden ? "show" : "hide" }} Задание 4</button><br />
  <p>&nbsp;&nbsp;&nbsp;&nbsp;</p>
  <p :class="obj">Задание 1</p>
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
p.hidden {
  display: none;
}
</style>