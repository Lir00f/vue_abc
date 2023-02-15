<script>
export default {
  data() {
    return {
      hrefs: [
        {href: '1.html', value: 'value1'},
        {href: '2.html', value: 'value2'},
        {href: '3.html', value: 'value3'},
		  ],
      sales: [
        {
          name: 'sale1',
          price: 1000,
          quantity: 11
        },
        {
          name: 'sale2',
          price: 2000,
          quantity: 6
        },
        {
          name: 'sale3',
          price: 5000,
          quantity: 5
        },
		  ]
    }
  },
  methods: {
    }
}
</script>
<template>
  Задание 1&nbsp;|&nbsp;
  <ul v-for="smh in hrefs">
    <li><a href="{{ smh.href }}">{{ smh.value }}</a></li>
  </ul>
  <br>Задание 2&nbsp;|&nbsp;
  <table v-for="sale in sales">
    <tr>
      <td>{{ sale.name }}</td>
      <td>{{ sale.price }}</td>
      <td>{{ sale.quantity }}</td>
    </tr>
  </table>
</template>
<style>
  table {
    display: flex;
    justify-content: flex-start;
    flex-direction: column-reverse;
  }
</style>

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