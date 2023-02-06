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
    arr1: ['x', 'y', 'z'], 
    arr2: [1, 2, 3],
    obj: {x: 1, y: 2, z: 3}, 
	}
},
methods: { 
 show: function() { 
  alert(today); 
 }
}
}
  let today = new Date(); 
</script>

<template>
  {{ show() }}
  <div>
		<h1> Vue exercises </h1>
	</div>
  <br>
  <img :src="attr">
  <div> <p> Hello, i'm {{ name }} {{ surn }}</p>
    <p>Check out my skills <a href="page.html">here</a></p> <br>
    <p class="sc">Квадрат num равен {{num*num}}, А сумма num1,num2,num3 равна {{num1+num2+num3}}.</p>
    <p class="sc"> Выведем каждую букву из массива в отдельной строке: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br> Теперь сумму элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
    <p class="sc">Выведем сумму элементов obj : {{obj.x + obj.y + obj.z}} </p>
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
