<template>
  <div>
    <h1>{{ name }}</h1>
    <input v-model="name" type="text">
  </div>
</template>

<script>
export default {
  data() {
    return {
      name: 'Igor',
    }
  },
}
</script>
