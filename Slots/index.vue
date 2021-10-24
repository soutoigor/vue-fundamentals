<template>
  <slots-example>
    This is the component's content.
    <template #footer="{ anything }" }>
      <button>Cancel</button>
      <button @click="mySubmitMethod(anything)">Send</button>
    </template>
  </slots-example>  
</template>

<script>
import SlotsExample from './Slots.vue'

export default {
  components: {
    SlotsExample,
  },
  methods: {
    mySubmitMethod(andThen) {
      alert('Do somethings first')
      andThen()
    },
  },
}
</script>
