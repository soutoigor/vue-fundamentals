<template>
  <div>
    <h1>Qual animal você prefere?</h1>
    <label for="dog">Cachorro</label>
    <input
      v-model="petImage"
      type="radio"
      id="dog"
      name="pet"
      value="https://i.guim.co.uk/img/media/fe1e34da640c5c56ed16f76ce6f994fa9343d09d/0_174_3408_2046/master/3408.jpg?width=1200&height=900&quality=85&auto=format&fit=crop&s=0d3f33fb6aa6e0154b7713a00454c83d"
    >
    <label for="cat">Gato</label>
    <input
      v-model="petImage"
      type="radio"
      id="cat"
      name="pet"
      value="https://thumbor.forbes.com/thumbor/fit-in/1200x0/filters%3Aformat%28jpg%29/https%3A%2F%2Fspecials-images.forbesimg.com%2Fimageserve%2F5de27c5d755ebf0006fbcf2e%2F0x0.jpg%3FcropX1%3D0%26cropX2%3D6016%26cropY1%3D311%26cropY2%3D3694"
    >
    <div>
      <img style="max-width: 300px" :src="petImage" >
    </div>
    <button :disabled="myList.length === 5" @click="myList.push(3)">adicionar</button>
    <h2>{{ myList }}</h2>
  </div>
</template>

<script>
export default {
  data() {
    return {
      petImage: '',
      myList: [],
    }
  },
}
</script>