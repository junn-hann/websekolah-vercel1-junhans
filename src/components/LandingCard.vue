<template>
 <main>
     <div class="car">
     <h1>Selamat Datang di Onlineshop ls reborn</h1>
 <p>Belanja gampang, sekolah senang.</p>
 <RouterLink to="/product">
    <button class="button";>lihat produk</button>
 </RouterLink>
 </div>
</main>
</template>
<style>
.car {
    text-align: center;
    margin-top: 25px;
    padding-top: 100px;
    display:block;
    flex-wrap: wrap;
   background:lightskyblue ;
   width: 100%;
   height: 250px;
   color: white;
   border-radius: 10px;
}
.button {
    background-color:lightskyblue;
    border-radius:999px ;
    color: purple;
}
</style>