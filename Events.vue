<template>
  <div>
    <h1>{{ num }}</h1>
    <h2>Estado do input {{ inputState }}</h2>
    <button @click="num += 1">Adicionar</button>
    <form @submit.prevent="inputState = 'submitou!'">
      <input @keyup.esc="inputState = 'esc!'" @focus="inputState = 'Focado'" @blur="inputState = 'Saiu!'" type="text">
      <button type="submit">submit!</button>
    </form>
  </div>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
      inputState: '',
    }
  },
}
</script>
