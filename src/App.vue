<script>
  export default {
    data() {
      return {
        brand: '',
        price: 0,
        count: 0,
        cars: {
          // brands: ['bmw', 'audi', 'mercedes'],
          BMW: 22000,
          mercedes: 23000,
          audi: 24000,
        },
      }
    },
  }
</script>

<template>
  <div class="main">
    <h1>hello {{ count }}</h1>
    <textarea v-on:change="brand = $event.target.value">brand</textarea>
    <textarea v-on:change="price = $event.target.value">price</textarea>
    <button v-on:click=";(cars[brand] = price), (brand = ''), (price = 0)">
      click me
    </button>
    <ul>
      <li v-for="(car, key) in cars" :key="key">{{ key }}: {{ car }}</li>
    </ul>
  </div>
</template>

<style></style>
