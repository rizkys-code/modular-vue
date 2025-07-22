    <template>
    <header class="header">
        <h2 class="header-judul">Rzkydev</h2>
        <nav class="navbar">
        <ul>
            <li><a href="#home-me">Home</a></li>
            <li><a href="#about-me">About</a></li>
            <li><a href="#experience-me">Experience</a></li>
            <li><a href="#skills-me">Skills</a></li>
            <li><a href="#project-me">Project</a></li>
        </ul>
        </nav>
    </header>
    </template>

    <script setup>
    // Tidak perlu script untuk saat ini
    </script>

    <style scoped>
    .header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px;
    border: 2px transparent;
    border-radius: 0 0 10px 10px;
    background: linear-gradient(90deg, #4e54c8, #8f94fb);
    font-family: "Poppins", sans-serif;
    }
    .header-judul {
    color: white;
    }
    .navbar ul {
    list-style: none;
    display: flex;
    gap: 20px;
    margin: 0;
    padding: 0;
    }
    .navbar a {
    text-decoration: none;
    color: white; /* Ubah warna agar terlihat di gradient */
    }
    .navbar a:hover {
    color: #ddd;
    }
    </style>