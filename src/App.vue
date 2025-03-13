<script>
  export default {
    data() {
      return {
        message: 'Vue',
        count: 0,
        cars: ['bmw', 'mercedess', 'audi'],
      }
    },
  }
</script>

<template>
  <div class="main">
    <h1>hello {{ count }}</h1>
    <textarea v-bind:placeholder="message"></textarea>
    <button v-on:click="cars.push(message)">click me</button>
    <ul>
      <li v-for="(car, idx) of cars" :key="idx">{{ car }}</li>
    </ul>
  </div>
</template>

<style></style>
