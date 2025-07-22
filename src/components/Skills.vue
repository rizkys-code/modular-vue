<template>
  <section id="skills-me" class="skills">
    <h2>Skills</h2>
    <p>The technologies I use to build powerful digital solutions, always moving forward.</p>
    <div class="skills-container">
      <div class="card">
        <!-- SVG HTML -->
        <h3><i><svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 256 256"><g fill="none"><rect width="256" height="256" fill="#e14e1d" rx="60"/><path fill="#fff" d="m48 38l8.61 96.593h110.71l-3.715 41.43l-35.646 9.638l-35.579-9.624l-2.379-26.602H57.94l4.585 51.281l65.427 18.172l65.51-18.172l8.783-98.061H85.824l-2.923-32.71h122.238L208 38z"/><path fill="#ebebeb" d="M128 38H48l8.61 96.593H128v-31.938H85.824l-2.923-32.71H128zm0 147.647l-.041.014l-35.579-9.624l-2.379-26.602H57.94l4.585 51.281l65.427 18.172l.049-.014z"/></g></svg></i> HTML</h3>
        <p>Keterampilan dalam membuat struktur halaman web yang semantik dan rapi.</p>
      </div>
      <div class="card">
        <h3><i class="fa-brands fa-css3-alt"></i> CSS</h3>
        <p>Kemampuan untuk mendesain dan menata halaman web menjadi lebih menarik dan responsif.</p>
      </div>
      <div class="card">
        <h3><i class="fa-brands fa-js"></i> JavaScript</h3>
        <p>Keahlian dalam membuat fungsionalitas dan interaktivitas pada halaman web.</p>
      </div>
    </div>
  </section>
</template>
<script setup></script>

<style scoped>
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
  grid-template-columns: repeat(3, 1fr); /* 3 kolom untuk skills */
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