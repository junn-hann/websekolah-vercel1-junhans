<script setup>
import AboutCard from '../components/AboutCard.vue';
</script>

<template>
    <main>
        <div class="balok">
            <h1>tentang kami</h1>
        </div>

<AboutCard/>

    </main>
</template>
<style scoped>
    .balok {
        color:white;
        width:100% ;
        height :100px;
        background:lightskyblue;
        overflow: hidden;
        margin: 10px;
        text-align: center;
        border-radius: 10px;
    }
</style>