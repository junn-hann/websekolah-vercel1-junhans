 <!-- <script setup>
defineProps(['nama', 'harga', 'gambar'])
</script>
<template>
 <div class="card">
 <img :src="gambar" :alt="nama" />
 <h3 style="color: lightblue;">{{ nama }}</h3>
 <button class="btn btn-grad">Rp {{ harga.toLocaleString('id-ID') }}</button>
 </div>
</template>
<style scoped>
.card {
 border: 1px solid #000000;
 border-radius: 10px;
 padding: 14px;
 width: 200px;
 text-align: center;
 background-color:blueviolet;
}
.card img {
 width: 100%;
 border-radius: 6px;
}
.btn-grad {
  background-image: linear-gradient(to right, #20002c 0%, #cbb4d4 51%, #20002c 100%);
}

.btn-grad {
  margin: 10px;
  padding: 15px 45px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: white;
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  display: block;
  outline: none;
  border: none;
}

.btn-grad:hover {
  background-position: right center;
  color: #fff;
  text-decoration: none;
}
</style> -->
<script setup> 
import { ref } from 'vue' 
  
defineProps(['nama', 'harga', 'gambar']) 
  
const gambarDipilih = ref(null) 
  
function bukaPreview(src) { 
  gambarDipilih.value = src 
} 
  
function tutupPreview() {
  gambarDipilih.value = null 
}
  function tambahKeKeranjang(nama){
    const suara = new Audio('/audio/notifikasi.mp3') 
    suara.play() 
    alert(`${nama} ditambahkan ke keranjang!`)
} 
</script> 
  
<template> 
  <div class="card"> 
    <img :src="gambar" :alt="nama" @click="bukaPreview(gambar)" /> 
    <h3>{{ nama }}</h3> 
    <p>Rp {{ harga.toLocaleString('id-ID') }}</p>
    <div class="btn-grad"> 
    <button @click="berhasildibeli(beli)">beli</button>  
  </div> 
    <button style="color: lightblue;" @click="tambahKeKeranjang(nama)">Tambah ke Keranjang</button> 
  </div> 
  
  <div v-if="gambarDipilih" class="preview-overlay" @click="tutupPreview"> 
    <img :src="gambarDipilih" class="preview-besar" /> 
  </div> 
</template> 
  
<style scoped> 
.card { 
  border: 1px solid #ddd; 
  border-radius: 10px; 
  padding: 14px; 
  width: 200px; 
  text-align: center;
  color: purple;
} 
.card img { width: 100%; border-radius: 6px; cursor: pointer; } 
  
.preview-overlay { 
  position: fixed; top: 0; left: 0; width: 100%; height: 100%; 
  background: rgba(0, 0, 0, 0.7); 
  display: flex; align-items: center; justify-content: center; 
  cursor: zoom-out; 
} 
.preview-besar { max-width: 80%; max-height: 80%; border-radius: 8px; } 
.btn-grad {
  background-image: linear-gradient(to right, #000000 0%, #0f9b0f 51%, #000000 100%);
}

.btn-grad {
  background-image: linear-gradient(to right, #20002c 0%, #cbb4d4 51%, #20002c 100%);
}

.btn-grad {
  margin: 15px;
  padding: 10px;
  text-align: center;
  text-transform: uppercase;
  transition: 0.5s;
  background-size: 200% auto;
  color: rgb(57, 144, 214);
  box-shadow: 0 0 20px #eee;
  border-radius: 10px;
  display: block;
  outline: none;
  border: none;
}

.btn-grad:hover {
  background-position: right center;
  color: #1e78ac;
  text-decoration: none;
}
button { 
  margin-top: 8px; 
  padding: 6px 12px; 
  border: none; 
  border-radius: 6px; 
  background: linear-gradient(to right, #20002c 0%, #cbb4d4 51%, #20002c 100%); 
  color: white; 
  cursor: pointer; 
} 
button:hover { background: #1F4E79; }
</style>