<script>
export default {
  data() {
    return {
      zadanie: "Задание",
      zadanie_number: 1,
    };
  },
  methods: {},
};
</script>
<template>
<input type="text" v-model="zadanie" />
<p>{{ zadanie }}</p>
<p>{{ zadanie.toUpperCase() }}</p>
<input type="number" v-model="zadanie_number" />
<p>{{ zadanie_number ** 2 }}</p>
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