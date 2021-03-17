<template>
  <div>
    <ul v-if="items.length > 1">
      <template
        v-for="num of items"
      >
        <li v-show="num % 2 === 0" :key="num">{{ num }}</li>
      </template>
    </ul>
    <h3 v-else-if="items.length === 1">
      O único item da lista é: {{ items[0] }}
    </h3>
    <h3 v-else>
      A lista está vazia :/
    </h3>
  </div>
</template>

<script>
export default {
  data() {
    return {
      items: [1, 2, 3, 4, 5, 6],
    }
  },
}
</script>