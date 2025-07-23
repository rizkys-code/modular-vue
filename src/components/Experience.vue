<template>
  <section id="experience-me" class="experience">
    <h2>Work Experience</h2>
    <div class="experience-container">
      <!-- v-for tetap di sini, tapi kita ganti div dengan komponen Card -->
      <Card v-for="(item, index) in items" :key="index">
        <!-- Semua konten ini akan dimasukkan ke dalam <slot> di Card.vue -->
        <h3>{{ item.title }}</h3>
        <p class="company">{{ item.company }}</p>
        <p>{{ item.description }}</p>
      </Card>
    </div>
  </section>
</template>

<script setup>
// 1. Impor komponen Card
import Card from './Card.vue'

// 2. Props tetap sama
defineProps({
  items: Array
})
</script>

<style scoped>
/* CSS di sini menjadi jauh lebih sedikit! Hanya untuk layout container. */
.experience {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  row-gap: 50px;
}
.experience-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  max-width: 800px;
}
@media (max-width: 768px) {
  .experience-container {
    grid-template-columns: 1fr;
  }
}
/* Class .company masih bisa di-style di sini jika perlu, atau dipindah ke global */
.company {
    font-family: "Poppins", sans-serif;
    color: #8f94fb;
    font-weight: 500;
}
</style>