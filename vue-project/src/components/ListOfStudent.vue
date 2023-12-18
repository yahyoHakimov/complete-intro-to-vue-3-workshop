<script>
export default {
  data() {
    return {
      amount: 10,
      incrementAmount: 5,
      message: 'Hi, Yahyo',
      userList: [
        {name: 'Yahyo'},
        {name: 'Asadbek'},
        {name: 'Otabek'},
        {name: 'Umidjon'},
        {name: 'Dilshod'},
        {name: 'Elyorjon'},
        {name: 'Rahimjon'}
      ]
    }
  },
  methods: {
    incrementCount() {
      return this.amount += this.incrementAmount;
    },
    decrementCount() {
      return this.amount -= this.incrementAmount
    }
  },
}
</script>

<template>
  <h1>Hello, Yahyo</h1>

  <ul v-for="users in userList">
    <li>{{users.name}}</li>
  </ul>

  <hr>

  <p>{{ message }}</p>

  <h1>{{ amount }}</h1>

  <button v-on:click="incrementCount">Increment Button</button>
  <button v-on:click="decrementCount">Decrement Button</button>
</template>