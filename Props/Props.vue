<template>
  <div class="badge" style="{ backgroundColor: color }">
    <span>{{ number }}</span>
  </div>
</template>

<script>
export default {
  props: {
    number: {
      type: Number,
      required: true,
    },
    color: {
      type: String,
      required: false,
      defaultValue: 'red',
    },
  },
}
</script>

<style scoped>
.badge {
  border-radius: 100%;
  padding: 3px;
  width: 5px;
  height: 5px;
}
</style>
