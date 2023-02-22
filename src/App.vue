<script>
export default {
  data() {
    return {
      newValue: "",
      items: ["a", "b", "c", "d", "e"],
    };
  },
  methods: {
    addValueEnd: function () {
      this.items.push(this.newValue);
    },
    addValueBegin: function () {
      this.items.unshift(this.newValue);
    },
  },
};
</script>
<template>
  <input v-model="newValue" />
  <button @click="addValueEnd">Добавить в конец</button>
  <button @click="addValueBegin">Добавить в начало</button>
  <ul v-for="(item, index) in items" :key="index">
    <li>
      {{ item }}
    </li>
  </ul>
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