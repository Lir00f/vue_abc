<script>
export default {
  data() {
    return {
      isDisabled: false,
    };
  },
  methods: {},
};
</script>
<template>
  <input
    type="checkbox"
    :checked="isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  />
  &nbsp;
  <button class="button"
    v-bind:disabled="!isDisabled"
    @click="($event) => (this.isDisabled = !this.isDisabled)"
  >
    {{ isDisabled ? "input включен" : "input выключен" }}
  </button>
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