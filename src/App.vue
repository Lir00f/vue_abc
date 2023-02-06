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
    date : '2',
	}
},
methods: { 
 show: function() { 
  alert(today); 
 },
 summ: function() {
  alert(this.num1 + this.num2)
 },
data: function(){
let date = this.dayOfWeek(this.date);
alert(date);
},
dayOfWeek: function(date){
let days = ['Monday', 'Tuesday', 'Wednesday', 'Thursday', 'Friday', 'Saturday', 'Sunday']
return days[date-1];
},
}
}
let today = new Date(); 
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
    <p class="sc"> Выведем каждую букву из массива в отдельной строке: <br> {{arr1[0]}} <br> {{arr1[1]}} <br> {{arr1[2]}} <br> Теперь сумму элементов второго массива : {{arr2[0] + arr2[1] + arr2[2]}}</p>
    <p class="sc">Выведем сумму элементов obj : {{obj.x + obj.y + obj.z}} </p>
    <button class="button button1" @click="show">Узнать дату(нажатие)</button>
    <button class="button button2" @mouseenter="show">Узнать дату(навестись)</button> <br>
    <button class="button button1" @click="date">Узнать день недели по числу({{ date }})</button>
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
