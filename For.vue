<template>
  <div>
    <ul>
      <li
        v-for="(item, index) of frameworks"
        :key="index"
      >
        {{ item }}
      </li>
    </ul>
    <ul>
      <li
        v-for="(value, property) in person"
        :key="property"
      >
        {{ property }} - {{ value }}
      </li>
    </ul>
    <button @click="frameworks.push('Express')">Adicionar</button>
  </div>
</template>

<script>
export default {
  data() {
    return {
      frameworks: ['Vue', 'React', 'Svelte', 'Angular'],
      person: {
        name: 'Igor',
        age: 23,
        height: '1.64',
      },
    }
  },
}
</script>
