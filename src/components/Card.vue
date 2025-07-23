<template>
  <div class="card">
    <!-- Di sinilah konten dari komponen induk akan disisipkan -->
    <slot></slot>
  </div>
</template>

<script setup>
// Komponen ini tidak butuh logic, hanya sebagai wadah.
</script>

<style scoped>
/* Semua gaya yang spesifik untuk kartu kita pindahkan ke sini */
.card {
   display: flex;
  flex-direction: column; /* <--- TAMBAHKAN BARIS INI */
  justify-content: flex-start;
  align-items: flex-start; /* Mulai dari kiri */
  text-align: left;
  padding: 20px;
  width: 100%;
  box-sizing: border-box;
  background-color: #ffffff;
  box-shadow: 0 4px 12px rgba(0, 0, 0, 0.08);
  border-radius: 12px;
  transition: transform 0.2s ease-in-out, box-shadow 0.2s ease-in-out;
}

.card:hover {
  transform: translateY(-5px);
  box-shadow: 0 8px 20px rgba(0, 0, 0, 0.12);
}
</style>