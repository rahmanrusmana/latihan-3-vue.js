<template>
    <div>
      <h2 v-if="umur >= 18">Selamat Datang, {{ nama }}!</h2>
      <p v-else>Maaf, kamu belum cukup umur.</p>
      <button @click="greet">Sapa Bro!</button>
    </div>
</template>
  

<script>
export default{
    nama: 'NewComponent',
    props: ['nama','umur'],

    methods:{
        greet(){
            alert('Hallo ' + this.nama)
        }
    }
    
}
</script>
