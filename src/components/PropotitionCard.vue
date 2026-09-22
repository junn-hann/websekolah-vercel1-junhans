<script setup>
defineProps (['icon','h1','h2'])
</script>
<template>
    <div class="container">
        <div class="icon">
            <p>{{ icon }}</p>
        </div>
            <h1>{{ h1 }}</h1>
            <p>{{ h2 }}</p>
    </div>
</template>
<style scoped>
.container{ 
  border: 1px solid #ddd; 
  border-radius: 10px; 
  padding: 14px; 
  width: 450px; 
  text-align: center;
  color: purple;
  margin-top: 20px;
} 
.icon {
    font-size: 2.5rem;
    margin-bottom:16px;
}
</style>