<script>
export default {
  data() {
    return {
      arr: ['a', 'b', 'd'],
    }
  },
  methods: {
    add: function() {
		  this.arr.push('b');
  },
    delFirst: function() {
      this.arr.shift();
  },
    delLast: function() {
      this.arr.pop();
  },
    delSecondToLast: function() {
      this.arr.splice(-2, 1);
  },
    sortArr: function() {
      this.arr.sort();
  },
    reverseOrder: function() {
      this.arr.reverse();
  }
}
}
</script>
<template>
  <button class="button" @click.once="add">1</button>
  <button class="button" @click.once="delFirst">2</button>
  <button class="button" @click.once="delLast">3</button>
  <button class="button" @click.once="delSecondToLast">4</button>
  <button class="button" @click.once="sortArr">5</button>
  <button class="button" @click.once="reverseOrder">6</button>
  <ul v-for="elem in arr">
    <li>{{ elem }}</li>
  </ul><br>
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