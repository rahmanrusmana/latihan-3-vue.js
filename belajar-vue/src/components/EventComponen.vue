<template>
    <div>
      <h2 v-if="umur >= 18">{{ pesanSelamat }}</h2>
      <p v-else>Maaf, kamu belum cukup umur.</p>
      <button @click="greet">Sapa Bro!</button>
      <slot name="footer"></slot>
    </div>
  </template>
  
  <script>
  import MyComponent from './MyComponent.vue';
  
  export default {
    components: {
      MyComponent
    },
    data() {
      return {
        nama: 'John',
        umur: 20
      };
    },
    methods: {
      onGreeted() {
        console.log('Kamu udah disapa, bro!');
        // Lakukan tindakan responsif lainnya...
      }
    }
  }
  </script>