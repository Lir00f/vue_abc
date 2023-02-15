<script>
export default {
  data() {
    return {
      isAdmin: true,
    }
  },
  methods: {
    toggle: function() {
      this.isAdmin = !this.isAdmin;
    }
  }
}
</script>
<template>
  <button class="button" @click="toggle">{{ isAdmin ? "Выдать админку" : "Забрать админку" }}</button><br>
  <p v-if="isAdmin">Пользователь сайта не являеется администратором</p>
  <p v-else>Вы администратор!</p>
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