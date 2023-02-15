<script>
export default {
  data() {
    return {
      vozrast: " ",
    }
  },
  methods: {
  }
}
</script>
<template>
  <h3>Введите ваш возраст: </h3><br>
  <input type="number" v-model.number="vozrast">
  <br>
  <p class="button" v-if="vozrast < 14">Вы ребенок</p>
  <p class="button"  v-else-if="vozrast < 18">Вы подросток</p>
  <p class="button"  v-else-if="vozrast < 25">Вы молодой человек</p>
  <p class="button"  v-else-if="vozrast <= 59">Вы взрослый человек</p>
  <p class="button"  v-else-if="vozrast >= 60">Вы пожилой человек</p>
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