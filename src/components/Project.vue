<!-- src/components/Project.vue -->

<template>
  <section id="project-me" class="project">
    <h2>Project</h2>
    <p>Berikut adalah beberapa proyek yang pernah saya kerjakan.</p>
    <div class="project-container">
      <div v-for="(project, index) in items" :key="index" class="card">
        <img :src="project.image" class="card-img-top" :alt="project.title" />
        <div class="card-body">
          <h4 class="card-title">{{ project.title }}</h4>
          <p class="card-text">{{ project.description }}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script setup>
defineProps({
  items: Array
})
</script>

<style scoped>
/* CSS tetap sama */
.project {
  display: flex;
  justify-content: center;
  align-items: center;
  text-align: center;
  flex-direction: column;
  gap: 50px;
}
.project-container {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
  width: 100%;
  max-width: 800px;
}
.card-img-top {
  width: 100%;
  border-top-left-radius: inherit;
  border-top-right-radius: inherit;
}
@media (max-width: 768px) {
  .project-container {
    grid-template-columns: 1fr;
  }
}
</style>