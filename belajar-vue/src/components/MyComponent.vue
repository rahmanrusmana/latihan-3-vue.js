<template>
    <div>
        <h2>Hallo Dunia</h2>
        <p>Ini Komponen Buatan Gue</p>
        <h2>Nama : {{ nama }}</h2>
        <p>Umur : {{ umur }}</p>
    </div>
  </template>
  
  <script>
  export default {
    nama: 'MyComponent', 
    props: ['nama', 'umur'],
    data() {
    return {
      message: 'Ini pesan dari komponen'
        };
    },
    methods: {
    greet() {
      console.log('Halo, bro!');
        }
    }
  }
  </script>
  
  <style>
    h2 {
        color: rgb(175, 96, 96);
    }

    p {
        font-size: 16px;
    }
    </style>
