<template>
  <section class="testimonial-section">
    <div class="container">
      <div class="header">
        <h2>Apa Kata Klien Kami</h2>
        <p>Dengarkan pengalaman langsung dari orang-orang yang telah menggunakan layanan kami.</p>
      </div>

      <!-- Testimonial Grid -->
      <div class="testimonial-grid">
        <div 
          v-for="item in testimonials" 
          :key="item.id" 
          class="testimonial-card"
        >
          <div class="card-content">
            <!-- Rating Stars -->
            <div class="rating">
              <span v-for="star in item.rating" :key="star">★</span>
            </div>

            <!-- Message -->
            <p class="message">"{{ item.message }}"</p>
          </div>

          <!-- User Info -->
          <div class="user-info">
            <img :src="item.avatar" :alt="item.name" class="avatar" />
            <div class="user-details">
              <h4>{{ item.name }}</h4>
              <p>{{ item.role }}</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
import { ref } from 'vue'

const testimonials = ref([
  {
    id: 1,
    name: 'resky syihahhhhh',
    role: 'Software Engineer',
    message: 'Layanan ini sangat membantu produktivitas tim kami. Interface-nya ramah pengguna dan fiturnya lengkap!',
    avatar: 'https://i.pravatar.cc/150?img=11',
    rating: 5
  },
  {
    id: 2,
    name: 'afgan syihapudinn',
    role: 'Product Manager',
    message: 'Dukungan pelanggan sangat responsif. Setiap ada kendala selalu terselesaikan dalam hitungan menit.',
    avatar: 'https://i.pravatar.cc/150?img=12',
    rating: 5
  },
  {
    id: 3,
    name: 'Deni syihah',
    role: 'UI/UX Designer',
    message: 'Desain dan pengalaman menggunakannya sangat intuitif. Sangat direkomendasikan untuk proyek skala besar.',
    avatar: 'https://i.pravatar.cc/150?img=13',
    rating: 4
  }
])
</script>

<style scoped>
/* Reset dasar & Section Container */
.testimonial-section {
  background-color: #f9fafb;
  padding: 60px 20px;
  font-family: Arial, sans-serif;
}

.container {
  max-width: 1100px;
  margin: 0 auto;
}

/* Header */
.header {
  text-align: center;
  margin-bottom: 40px;
}

.header h2 {
  font-size: 2rem;
  color: #111827;
  margin-bottom: 10px;
}

.header p {
  font-size: 1.1rem;
  color: #6b7280;
  margin: 0;
}

/* Grid Layout */
.testimonial-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
}

/* Media Query untuk Tablet & Desktop (Responsif) */
@media (min-width: 640px) {
  .testimonial-grid {
    grid-template-columns: repeat(2, 1fr);
  }
}

@media (min-width: 1024px) {
  .testimonial-grid {
    grid-template-columns: repeat(3, 1fr);
  }
}

/* Testimonial Card */
.testimonial-card {
  background-color: #ffffff;
  border-radius: 12px;
  padding: 24px;
  box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1), 0 2px 4px -1px rgba(0, 0, 0, 0.06);
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  transition: transform 0.2s ease, box-shadow 0.2s ease;
}

.testimonial-card:hover {
  transform: translateY(-4px);
  box-shadow: 0 10px 15px -3px rgba(0, 0, 0, 0.1), 0 4px 6px -2px rgba(0, 0, 0, 0.05);
}

/* Content */
.card-content {
  margin-bottom: 20px;
}

.rating {
  color: #f59e0b;
  font-size: 1.2rem;
  margin-bottom: 12px;
}

.message {
  color: #4b5563;
  font-style: italic;
  line-height: 1.6;
  margin: 0;
}

/* User Info */
.user-info {
  display: flex;
  align-items: center;
  border-top: 1px solid #e5e7eb;
  padding-top: 16px;
}

.avatar {
  width: 48px;
  height: 48px;
  border-radius: 50%;
  object-fit: cover;
  margin-right: 16px;
}

.user-details h4 {
  margin: 0;
  font-size: 1rem;
  color: #111827;
}

.user-details p {
  margin: 4px 0 0 0;
  font-size: 0.875rem;
  color: #6b7280;
}
</style>