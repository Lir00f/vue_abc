<script>
export default {
  data() {
    return {
      value: "",
      value_button: "",
      value_array: "",
    };
  },
  methods: {
    split_value: function () {
      this.value_array = this.value_button.split(" ");
    },
  },
};
</script>
<template>
 <valuearea v-model="value"></valuearea>
  &nbsp;
  <p>{{ value }}</p>
  &nbsp;
  <valuearea v-model="value_button"></valuearea>
  &nbsp;
  <button class="button" @click="split_value">Массив</button>
  &nbsp;
  <ul v-for="elem in value_array">
    <li :key="key">
      {{ elem }}
    </li>
  </ul>
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