<script>
  export default {
    data() {
	return {
    cost: '50',
    amount: '3',
    price: 'Press to compute the price',
		name: 'Shadow',
		surn: 'Fiend',
    attr: 'sf.gif',
    text: 'page',
		href: 'page.html',
	}
},
methods: {
    computePrice: function() {
      this.price = (this.cost * this.amount);
    }
  }
}
let today = new Date(); 
</script>

<template>
  <div>
		<h1> Vue exercises </h1>
	</div>
  <br>
  <img width="500" height="500" :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
  <p>Check out my skills <a href="page.html">here</a></p> <br>
  <p>Enter number for cost:</p>
  <input type="number" v-model.number="cost" ref="costField">
  <p>Enter number for amount:</p>
  <input type="number" v-model.number="amount" ref="amountField">
  <button class="button" k="computePrice">{{ price }}</button>
  </div>
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

.button1 {
    box-shadow: 0 8px 16px 0 rgba(0,0,0,0.2), 0 6px 20px 0 rgba(0,0,0,0.19);
}

.button2:hover {
    box-shadow: 0 12px 16px 0 rgba(255, 255, 255, 0.24),0 17px 50px 0 rgba(255, 255, 255, 0.19);
}

header {
  line-height: 1.5;
}

.sc {
  font-size: medium;
 color: aqua;
}

p {
  line-height: 1.4;
  font-size: large;
  letter-spacing: 2px;
  font-family: 'Gill Sans', 'Gill Sans MT', Calibri, 'Trebuchet MS', sans-serif;
  color: rgb(255, 0, 0);
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
