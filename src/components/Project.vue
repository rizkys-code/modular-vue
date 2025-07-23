<!-- src/components/Project.vue -->

<template>
  <section id="project-me" class="project">
    <h2>Project</h2>
    <p>Berikut adalah beberapa proyek yang pernah saya kerjakan.</p>
    <div class="project-container">
      <!-- Ganti div dengan Card -->
      <Card v-for="(project, index) in items" :key="index">
        <img :src="project.image" class="card-img-top" :alt="project.title" />
        <div class="card-body">
          <h4 class="card-title">{{ project.title }}</h4>
          <p class="card-text">{{ project.description }}</p>
        </div>
      </Card>
    </div>
  </section>
</template>

<script setup>
import Card from './Card.vue'

defineProps({
  items: Array
})
</script>

/* src/components/Project.vue */

<style scoped>
/* KEMBALIKAN GAYA UNTUK SECTION UTAMA */
.project {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
  font-family: "Poppins", sans-serif;
  gap: 50px;
}

/* KEMBALIKAN GAYA UNTUK GRID CONTAINERNYA */
.project-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  max-width: 800px;
}

/* GAYA RESPONSIVENESS-NYA JUGA */
@media (max-width: 768px) {
  .project-container {
    grid-template-columns: 1fr;
  }
}

/* --- Gaya untuk konten di dalam card yang sudah benar bisa tetap di sini --- */
.card-img-top {
  width: 100%;
  height: auto;
  object-fit: cover;
  border-top-left-radius: 12px; 
  border-top-right-radius: 12px;
  margin-bottom: 15px;
}

.card-body {
  padding: 0 5px 5px 5px;
}
</style>