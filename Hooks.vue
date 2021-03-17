<template>
  <h1>Hooks: {{ num }}</h1>
</template>

<script>
export default {
  data() {
    return {
      num: 0,
    }
  },
  beforeCreate() {
    console.log('beforeCreate')
  },
  created() {
    console.log('created')
  },
  beforeMount() {
    console.log('beforeMount')
  },
  mounted() {
    console.log('mounted')
    setInterval(() => {
      this.num += 1
    }, 1000)
  },
  updated() {
    console.log('updated')
  },
  beforeDestroy() {
    console.log('beforeDestroy')
    alert('Vai destruir ')
  },
}
</script>
