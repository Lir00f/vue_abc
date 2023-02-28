<script>
export default {
    emits: ['show', 'show1'],
    data() {
        return {
        }
    },
    methods: {
        handleName() {
            this.$emit('show', 'Milana Prikolovna');
        },
        handleSalary(){
            this.$emit('show1', 'Polina Bebrusova', '15999');
        }
    }
}
</script>

<template>
<button class="button" @click="handleName">Имя</button>
<button class="button" @click="handleSalary">Зарплата</button>
</template>

<style>
p {
    font-size: 1cm;
    text-align: center;
  text-shadow:
    1px 1px 1px silver,
    -1px 1px 1px silver;
  color: white;
  transition: all .5s;
}

p:hover {
    text-align: center;
    font-size: 1.2cm;
  text-shadow:
    -1px -1px 1px rgb(252, 1, 1),
    1px -1px 1px rgb(252, 1, 1);
  color: rgb(165, 145, 238);
}

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
</style>