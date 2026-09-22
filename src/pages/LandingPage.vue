
<script setup>
    import LandingCard from '../components/LandingCard.vue'
    import PropotitionCard from '../components/PropotitionCard.vue';
    const daftarPropotition = [
        { id: 1,
        icon: '👑', 
        h1: 'kualitas terjamin',
        h2:'bahan di pilih langsung dengan kualitas terbaik' },
        { id: 2,
        icon: '✨',
        h1: 'harga bersahabat',
        h2:'harga terjangkau untuk semua pelajar' },
        { id: 3,
         icon: '🎇', 
         h1: 'ambil di sekolah',
         h2:'pesanan dapat di ambil di sekolah' },
    ]
</script>
<template>
    <main>
        <LandingCard/>
        <div class="balok">
        <video controls width="480" muted loop>
            <source src="/video/promo-toko.mp4" type="video/mp4" />
        </video>
        </div>
        <div class="grid">
            <PropotitionCard
            v-for="propotition in daftarPropotition"
            :key="propotition.id"
            :icon="propotition.icon"
            :h1="propotition.h1"
            :h2="propotition.h2"
            />
        </div>
    </main>
    </template>
    <style scoped>
        .grid {
            display: flex;
            gap: 20px;
            place-content: center;
            flex-wrap: wrap;
            }
            .balok {
                text-align: center;
            }
            </style>
