<template>
  <div>
   <h2>Formulir data</h2>
    <form @submit.prevent="submitForm">
      <label for="nama">Nama : </label>
      <input type="text" id="nama" v-model="data.nama"> <br>

      <label for="kelas">Kelas : </label>
      <input type="text" id="kelas" v-model="data.kelas" > <br>
      
      <label for="alamat">alamat : </label>
      <input type="text" id="alamat" v-model="data.alamat" > <br>

      <label for="nilaimtk">nilaimtk : </label>
      <input type="number" id="nilaimtk" v-model="data.nilaimtk" > <br>

      <label for="nilaiindo">nilaiindo : </label>
      <input type="number" id="nilaiindo" v-model="data.nilaiindo" > <br>

      <label for="nilaiipa">nilaiipa : </label>
      <input type="number" id="nilaiipa" v-model="data.nilaiipa" > <br>

      <button type="submit">Kirim</button>
    </form>
  </div>
  <div id="a"></div>
</template>

<script>

export default {
  data() {
    return {
      data: {
        nama: '',
        kelas: '',
        alamat: '',
        nilaimtk: '',
        nilaiindo: '',
        nilaiipa : '',
      },
    };
  },

  

  methods: {

    submitForm() {
      // Lakukan sesuatu dengan data data
      this.total = parseInt(this.data.nilaimtk)+
      parseInt(this.data.nilaiindo)+ parseInt(this.data.nilaiindo)

      if(this.total > 240){
        this.keterangan = "Lulus"
      } else{
        this.keterangan = "Tidak Lulus"
      }

      document.getElementById('a').innerHTML = ("Nama : " + this.data.nama)
       + ("<br>kelas : " + this.data.kelas)  + ("<br>Alammat : " + this.data.alamat)
       + ("<br>Nilai Matematika : " + this.data.nilaimtk) + ("<br>Nilai Indonesia : " + this.data.nilaiindo)
       + ("<br>Nilai IPA : " + this.data.nilaiipa)+ ("<br>Total : " + this.total)
       + ("<br>Keterangan : " + this.keterangan);
      
      
      
    },
  },
};


</script>