<template>
  <div id="app">
    <Navbar /> <!-- Pastikan komponen Navbar digunakan di sini -->
    <router-view /> <!-- Ini akan menampilkan komponen yang sesuai dengan rute saat ini -->
  </div>
</template>

<script>
import Navbar from './components/navbar.vue'; // Pastikan path ini benar

export default {
  components: {
    Navbar // Daftarkan komponen Navbar di sini
  }
};
</script>

<style>
/* Gaya Anda di sini */
</style>
