<script>
export default {
  data() {
    return {
      brand: '',
      price: 0,
      cars: {
        BMW: 22000,
        mercedes: 23000,
        audi: 24000,
      },
    }
  },

  methods: {
    addCar() {
      if (this.brand === '' || this.price === 0) return
      this.cars[this.brand] = this.price
      this.brand = ''
      this.price = 0
    },
  },
}
</script>

<template>
  <div class="main">
    <textarea :value="brand" v-on:input="brand = $event.target.value">
    </textarea>

    <textarea :value="price" v-on:input="price = $event.target.value">
    </textarea>

    <button v-on:click="addCar">click me</button>
    <ul>
      <li v-for="(car, key) in cars" :key="key">{{ key }}: {{ car }}</li>
    </ul>
  </div>
</template>

<style></style>
