<template>
  <section id="experience-me" class="experience">
    <h2>Work Experience</h2>
    <div class="experience-container">
      <div class="card">
        <h3>Laborartorium ICT Terpadu</h3>
        <p class="company">Laborartorium ICT Terpadu | 2025 - Present</p>
        <p>
          Assisted students during lab sessions, maintained lab equipment, and provided solutions for basic technical issues encountered during practicals.
        </p>
      </div>
      <div class="card">
        <h3>Budi Luhur IT Club</h3>
        <p class="company">Budi Luhur IT CLUB | 2025 - Present</p>
        <p>
          Assisted students during lab sessions, maintained lab equipment, <br />
          and provided solutions for basic technical issues encountered during practicals.
        </p>
      </div>
    </div>
  </section>
</template>

<script setup></script>

<style scoped>
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

/* Responsiveness untuk layar kecil */
@media (max-width: 768px) {
  .experience-container {
    grid-template-columns: 1fr;
  }
}
</style>