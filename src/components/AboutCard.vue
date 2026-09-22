<script setup>
// defineProps(['a1''a2''a3'])
</script>

<template>
    <div class="ca">
        <div class="ci">
            <h1 style="color:lightskyblue">cerita kami</h1>
            <p>kami adalah online shop yang hadir untuk menyediakan berbagai produk berkualitas dengan harga yang terjangkau.
                 Kami berkomitmen untuk memberikan pengalaman belanja yang mudah, aman, dan nyaman bagi setiap pelanggan.
                 Kami selalu berusaha memilih produk terbaik, memberikan pelayanan yang ramah dan responsif, 
                 serta memastikan setiap pesanan diproses dengan teliti. Kepuasan pelanggan adalah prioritas utama kami.</p>
                 <P>kami berharap online shop ini tidak menjadi sebuah proyek sekolah, tetapi menjadi langkah awal untuk harus bekarya,belajar,dan mengembangkan kemampuan di bidand teknologi digital</P>
        </div>
        <div class="gambar">
            <img src="/gambar/sepatu-fuksal.png" alt="toko">
        </div>
    </div>
</template>
<style scoped>
.ca{
    display: flex;
    align-items:flex-start;
    margin:50px;
    flex:1;
    flex-direction: row;
    overflow: hidden;
}
.ci{
    flex:1;
}
.gambar img{
    width:250px;
    height: auto;
    border-radius: 10px;
}

</style>