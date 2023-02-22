<script>
export default {
  data() {
    return {
      choice: "",
      english: true,
      russian: false,
      python: false,
    };
  },
  methods: {
    eng: function () {
      this.english = true;
      this.russian = false;
      this.python = false;
    },
    rus: function () {
      this.english = false;
      this.russian = true;
      this.python = false;
    },
    py: function () {
      this.english = false;
      this.russian = false;
      this.python = true;
    },
  },
};
</script>
<template>
<p v-if="english">What is your mother tongue?</p>
  <p v-if="russian">Какой ваш родной язык?</p>
  <p v-if="python">
    print('hello world!') :)
  </p>
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="English"
    @click="eng"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="Русский"
    @click="rus"
  />
  &nbsp;
  <input
    name="radio"
    type="radio"
    v-model="choice"
    value="def def def"
    @click="py"
  />
  &nbsp;
  <p>{{ choice }}</p>
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