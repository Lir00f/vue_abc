<script>
export default {
  data() {
    return {
      den: "if you see this then something went wrong",
    }
  },
  methods: {
    denOfTheWeek: function() {
    this.den = new Date().getDay();
  },
}
}
</script>
<template>
  <button class="button" @click="denOfTheWeek">тык</button><br>
  <p v-if="this.den === 1">Понедельник</p>
  <p v-if="this.den === 2">Вторник</p>
  <p v-if="this.den === 3">Среда</p>
  <p v-if="this.den === 4">Четверг</p>
  <p v-if="this.den === 5">Пятница</p>
  <p v-if="this.den === 6">Суббота</p>
  <p v-if="this.den === 0">Воскресенье</p>
</template>

<style >
.button {
    background-color: #00eeff; /* Green */
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
</style>