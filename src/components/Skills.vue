<!-- src/components/Skills.vue -->

<template>
  <section id="skills-me" class="skills">
    <h2>Skills</h2>
    <p>The technologies I use to build powerful digital solutions, always moving forward.</p>
    <div class="skills-container">
      <!-- Ganti div dengan Card -->
      <Card v-for="(skill, index) in items" :key="index">
        <h3>
          <i v-if="skill.icon" v-html="skill.icon"></i>
          <i v-if="skill.iconClass" :class="skill.iconClass"></i>
          {{ skill.name }}
        </h3>
        <p>{{ skill.description }}</p>
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

<style scoped>
/* Lagi-lagi, CSS jadi lebih simpel */
.skills {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  row-gap: 50px;
  background-color: #ededed;
}
.skills-container {
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
  width: 100%;
  max-width: 900px;
}
@media (max-width: 768px) {
  .skills-container {
    grid-template-columns: 1fr;
  }
}
</style>