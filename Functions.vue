<template>
  <div>
    <h1>Methods</h1>
    {{ total }}
    <button @click="sum(2, 2)">sum</button>
    <h2 style='border: 1px solid #f00;'>Nome inteiro: {{ fullName }}</h2>
    <input v-model="firstName" type="text">
    <h3>{{ items }}</h3>
    <button :disabled="shouldDisableButton" @click="addItem(8)">Add</button>
    <h3>Watch: {{ number }}</h3>
    <button @click="number = Math.floor(Math.random() * 6 ) + 1">Add watch</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      total: 0,
      firstName: 'Igor',
      lastName: 'Souto',
      items: [1, 2, 3],
      number: 1,
   }
  },
  methods: {
    showInConsole(value) {
      console.log(value)
    },
    addItem(value) {
      this.items.push(value)
    },
    sum(num1, num2) {
      this.total = num1 + num2
      this.showInConsole('Calculou!!!')
    },
    isEven(number) {
      return number % 2 === 0
    },
  },
  computed: {
    fullName() {
      return `${this.firstName} ${this.lastName}`
    },
    shouldDisableButton() {
      return this.items.length === 5
    },
  },
  watch: {
    number(value, oldValue) {
      if (this.isEven(value) && this.isEven(oldValue)) {
        alert('Parabéns, você tirou dois números seguidos pares!')
        this.number = 0
      }
    },
  },
}
</script>
