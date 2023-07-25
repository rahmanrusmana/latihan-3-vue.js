<template>
    <div>
        <!-- <h1>{{ text }}</h1> -->
        <my-component nama="Jhon" umur="25"></my-component>
        <hr>
        <!-- <new-component umur = "18" nama = "Rahman"></new-component> -->
        <latihan-componen></latihan-componen>
        <hr>
        <watchers-componen nama="Rahman" umur="80"></watchers-componen>
        <hr>
        <h2>Komponen Event</h2>
        <event-componen nama="" umur="umur" @greeted="onGreeted">
            <template #footer>
                <div>
                    <p>Ini Adalah Footer</p>
                </div>
            </template>
        </event-componen>
        <hr>
        <header ></header>
        <hr>
        
    </div>
  </template>
  
  <script setup>
  import MyComponent from './MyComponent.vue';
  import Header from './Header.vue'
  import WatchersComponen from './WatchersComponen.vue';
  import latihanComponen from './latihanComponen.vue';
  import EventComponen from './EventComponen.vue';

  // export default {
  //   nama: 'Header', 
  //   props: ['text']
  //   }
  </script>
  
  <style>
    /* h1 {
        color: rgb(0, 0, 0);
        background-color: aquamarine;
        text-align: center;
    }

    p {
        font-size: 16px;
    } */
    </style>
