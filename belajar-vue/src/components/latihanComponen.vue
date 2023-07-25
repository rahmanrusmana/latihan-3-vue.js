<template>
    <div>
        <input type="text" v-model="cari" cari="cariData"
         placeholder="Cari Data">
        <ul v-if="cari.length === 0">
      <li v-for="item in cariData" v:key="item.id">{{ item.tittle }} -
         {{ item.price }}</li>
    </ul>
    <P v-else="cari">Data Tidak Ada</P>
    </div>
</template>

<script>
    export default{
        data() {
            return {
                cari: '',
                produc: [] 
            }
        },
        created() {
            this.produc = [
                {id: 1, tittle: "Baju Anak", price: 25000},
                {id: 2, tittle: "Susu Anak", price: 75000},
                {id: 3, tittle: "Topi", price: 1000},
                {id: 4, tittle: "Balon", price: 100},
                {id: 5, tittle: "Kinder Joy", price: 1500}
            ]
        },
        computed: {
            cariData(){
                return this.produc.filter((item) =>{
                    return item.tittle.match(this.cari);
                })
            }
        }
    }
</script>