<script>
export default {
    props: {
        id: Number,
        name: String,
        surn: String,
    },
    emits: ['change'],
    data() {
        return {
            isEdit: false,
            newName: this.name,
            newSurn: this.surn,
        }
    },
    methods: {
        edit(){
            this.isEdit = true;
        },
        save(){
            this.isEdit = false;
            this.$emit('change', this.id, this.newName, this.newSurn);
        }
    }
}
</script>

<template>
    <template v-if="!isEdit">
    <p class="developer">{{ name }} {{ surn }}</p>
    <button class="button" @click="edit">Edit</button>
</template>
    <template v-else>
        <input class="text-field__input" v-model="newName">
        <input class="text-field__input" v-model="newSurn">
        <button class="button" @click="save">Save</button>
    </template>
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
    -1px -1px 1px rgb(252, 93, 1),
    1px -1px 1px rgb(252, 93, 1);
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