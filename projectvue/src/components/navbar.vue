<template>
  <nav>
    <ul>
      <li><router-link to="/" class="nav-link">Kalkulator</router-link></li>
      <li><router-link to="/about" class="nav-link">Tentang</router-link></li>
      <li><router-link to="/beranda" class="nav-link">Beranda</router-link></li>
    </ul>
  </nav>
</template>

<script setup>
import { RouterLink } from 'vue-router';
</script>

<style scoped>
nav {
  font-size: 30px;
  line-height: 1.6;
  font-style: bold;
  font-family:  'Gill Sans', 'Gill Sans MT', 'Calibri', 'Trebuchet MS', sans-serif;
  background-color: #fdf9fa; /* Warna latar belakang */
  color: #fff; /* Warna teks */
  padding: 10px 0; /* Padding untuk jarak */
  text-align: center; /* Pusatkan teks */
  box-shadow: 0 4px 8px rgba(0, 0, 0, 0.1); /* Shadow untuk efek kedalaman */
}

ul {
  display: flex; /* Gunakan Flexbox untuk layout */
  justify-content: center; /* Pusatkan item secara horizontal */
  align-items: center; /* Pusatkan item secara vertikal */
  list-style-type: none; /* Hapus gaya default list */
  padding: 0; /* Hapus padding */
  margin: 0; /* Hapus margin */
}

li {
  margin: 0 15px; /* Jarak antar item */
}

.nav-link {
  color: rgb(19, 18, 18); /* Warna link */
  text-decoration: none; /* Hapus garis bawah */
  padding: 10px 15px; /* Padding dalam link */
  border-radius: 5px; /* Sudut bulat */
  transition: background-color 0.3s; /* Transisi smooth */
}

.nav-link:hover {
  background-color: #f8f4f6; /* Warna latar belakang lebih gelap saat hover */
}
</style>
