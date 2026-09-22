<script setup>
import ProductCard from '../components/ProductCard.vue'
const daftarProduk = [
 { id: 1, nama: 'ls reborn green ', harga: 600000, gambar:
'https://topsystem.id/api/product/600/specs_galactica_morph_nv_jr_in_icicle_evergreen_419.webp' },
 { id: 2, nama: 'ls reborn silver black', harga: 550000, gambar:
'https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRSf7XQBMhaIqzlcZ9Z8IGHVljFFIIVpyMwViZmkur8HA&s' },
 { id: 3, nama: 'ls reborn ungu', harga: 1200000, gambar:
'https://images.tokopedia.net/img/cache/700/aphluv/1997/1/1/740ab4925d844cfaa6427961003eeb45~.jpeg.webp' },
]
</script>
<template>
 <main>
    <div class="balok">
 <h1>produk kami</h1>
 </div>
 <div class="grid">
 <ProductCard
 v-for="produk in daftarProduk"
 :key="produk.id"
 :nama="produk.nama"
 :harga="produk.harga"
 :gambar="produk.gambar"
 />
 </div>
 </main>
</template>
<style scoped>
.grid {
 display: flex;
 gap: 16px;
 flex-wrap: wrap;
}
</style>