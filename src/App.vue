<script>
  export default {
    data() {
	return {
		name: 'Shadow',
		surn: 'Fiend',
    attr: 'sf.gif',
    text: 'page',
		href: 'page.html',
    num: 5,
    num1: 1,
		num2: 2,
		num3: 3,
	}
}
  }
</script>

<template>
  <div>
		<h1> Vue exercises </h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
    <p>Check out my skills <a href="page.html">here</a></p> <br>
    <p class="sc">Квадрат num равен {{num*num}}, А сумма num1,num2,num3 равна {{num1+num2+num3}}.</p>

  </div>
</template>

<style >

header {
  line-height: 1.5;
}

.sc {
  font-size: medium;
 color: aqua;
}

p {
  line-height: 2.5;
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
