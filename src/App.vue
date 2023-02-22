<script>
export default {
  data() {
    return {
      num: 1,
      num_square: "Задание 1",
      numero_uno: 0,
      numero_dos: 0,
      sum_num: "Задание 2",
      text_uno: "placeholder",
      text_dos: "placeholder",
      fullName: "",
      userName: "",
      userSurname: "",
      userPatronymic: "",
    };
  },
  methods: {
    square: function () {
      this.num_square = this.num ** 2;
    },
    sum: function () {
      this.sum_num = this.numero_uno + this.numero_dos;
    },
    swap: function () {
      const temp = this.text_uno;
      this.text_uno = this.text_dos;
      this.text_dos = temp;
    },
    split: function () {
      this.userSurname = this.fullName.split(" ")[0];
      this.userName = this.fullName.split(" ")[1];
      this.userPatronymic = this.fullName.split(" ")[2];
    },
  },
};
</script>
<template>
<input type="num" v-model="num" />
  <button @click="square">Квадрат num</button>
  &nbsp;
  <p>{{ num_square }}</p>
  &nbsp;
  <input type="num" v-model="numero_uno" />
  <input type="num" v-model="numero_dos" />
  <button @click="sum">Сумма</button>
  &nbsp;
  <p>{{ sum_num }}</p>
  &nbsp;
  <input type="text" v-model="text_uno" />
  <input type="text" v-model="text_dos" />
  <button @click="swap">Замена</button>
  &nbsp;
  <input type="text" v-model="fullName" />
  <button @click="split">Поделить ФИО</button>
  <p>Фамилия = {{ userSurname }}</p>
  <p>Имя = {{ userName }}</p>
  <p>Отчество = {{ userPatronymic }}</p>
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