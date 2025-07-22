<template>
  <section id="home-me" class="home">
    <div class="text-center hero-image">
      <!-- Path ke gambar di folder public -->
      <img src="/img/profile.jpeg" class="rounded" alt="Profile Picture" />
    </div>
    <h1>Hello Im Rizky Saputra</h1>
    <p>
      I'm passionate about technology, web development, and UI/UX design. <br />
      Currently studying at Budi Luhur University.
    </p>
  </section>
</template>

<script setup></script>

<style scoped>
.home {
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
  text-align: center;
  gap: 10px;
  padding: 20px;
  margin: 0; /* Hapus margin atas/bawah agar lebih rapi saat digabung */
}
.rounded {
  width: 200px;
  height: 200px;
  object-fit: cover;
  border-radius: 50%;
  margin: 10px;
}
.hero-image {
  margin: 0;
  margin-bottom: 20px;
}
</style>