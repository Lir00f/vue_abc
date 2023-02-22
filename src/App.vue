<script>
export default {
  data() {
    return {
      lang: [],
    };
  },
  methods: {},
};
</script>
<template>
<input type="checkbox" v-model="lang" value="c" />
  &nbsp;
  <p>C</p>
  &nbsp;
  <input type="checkbox" v-model="lang" value="python" />
  &nbsp;
  <p>Python</p>
  <input type="checkbox" v-model="lang" value="javascript" />
  &nbsp;
  <p>JavaScript</p>
  &nbsp;
  <ul v-for="elem in lang">
    <li>{{ elem }}</li>
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