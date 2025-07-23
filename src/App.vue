<script setup>
// Bagian 1: Import 'ref' dari Vue untuk membuat data menjadi reaktif
import { ref } from 'vue'

// Import semua komponen yang sudah kita buat
import Header from './components/Header.vue'
import Home from './components/Home.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Skills from './components/Skills.vue'
import Project from './components/Project.vue'

// --- PUSAT KENDALI DATA ---
// Semua konten portofolio didefinisikan di sini.
// Kita membungkusnya dengan ref() agar Vue bisa melacak jika ada perubahan.

// Data untuk bagian Pengalaman Kerja
const experiences = ref([
  {
    title: 'Laboratorium ICT Terpadu',
    company: 'Laboratorium ICT Terpadu | 2025 - Present',
    description: 'Membantu mahasiswa selama sesi lab, merawat peralatan lab, dan memberikan solusi untuk masalah teknis dasar yang dihadapi selama praktikum.'
  },
  {
    title: 'Budi Luhur IT Club',
    company: 'Budi Luhur IT CLUB | 2025 - Present',
    description: 'Berkontribusi dalam berbagai proyek desain dan pengembangan sebagai Junior Design Engineer, membantu sesama anggota dalam belajar dan berkembang.'
  }
])

// Data untuk bagian Skills
const skills = ref([
  {
    
    icon: '<svg xmlns="http://www.w3.org/2000/svg" width="50" height="50" viewBox="0 0 256 256"><g fill="none"><rect width="256" height="256" fill="#e14e1d" rx="60"/><path fill="#fff" d="m48 38l8.61 96.593h110.71l-3.715 41.43l-35.646 9.638l-35.579-9.624l-2.379-26.602H57.94l4.585 51.281l65.427 18.172l65.51-18.172l8.783-98.061H85.824l-2.923-32.71h122.238L208 38z"/><path fill="#ebebeb" d="M128 38H48l8.61 96.593H128v-31.938H85.824l-2.923-32.71H128zm0 147.647l-.041.014l-35.579-9.624l-2.379-26.602H57.94l4.585 51.281l65.427 18.172l.049-.014z"/></g></svg>',
    name: 'HTML',
    description: 'Keterampilan dalam membuat struktur halaman web yang semantik dan rapi.'
  },
  {
    
    iconClass: 'fa-brands fa-css3-alt',
    name: 'CSS',
    description: 'Kemampuan untuk mendesain dan menata halaman web menjadi lebih menarik dan responsif.'
  },
  {
    iconClass: 'fa-brands fa-js',
    name: 'JavaScript',
    description: 'Keahlian dalam membuat fungsionalitas dan interaktivitas pada halaman web.'
  }
])

// Data untuk bagian Proyek
const projects = ref([
  {
    // Pastikan path ini benar menuju gambar di folder public/img/
    image: '/img/LAB.png',
    title: 'Website Informasi Masjid At-Taqwa',
    description: 'Membuat website profil dan sistem informasi untuk Masjid At-Taqwa menggunakan HTML, CSS, dan PHP.'
  },
  {
    image: '/img/Martabak.png',
    title: 'Desain UI/UX Aplikasi Mobile',
    description: 'Merancang antarmuka pengguna untuk aplikasi mobile pemesanan makanan dengan Figma.'
  }
])
</script>

<template>
  <Header />
  <main>
    <!-- Komponen ini masih statis, tidak perlu data dari sini -->
    <Home />
    <About />

    <!-- Bagian 2: Mengirim data ke komponen anak menggunakan "props" -->
    <!-- ":items" adalah cara mengirim data. "experiences" adalah data yang dikirim. -->
    <Experience :items="experiences" />
    <Skills :items="skills" />
    <Project :items="projects" />
    

  </main>
  <!-- Kamu bisa menambahkan komponen Footer di sini nantinya -->
</template>

<style>
/* Gaya global yang tidak di-scope bisa diletakkan di sini atau di main.css */
/* Kita sudah memindahkannya ke src/assets/main.css, jadi di sini bisa dikosongkan */
</style>